# daemonSet

 A DaemonSet ensures a copy of a Pod is running across a set of nodes in a Kubernetes cluster. DaemonSets share similar functionality with ReplicaSets; both create Pods that are expected to be long-running services and ensure that the desired state and the observed state of the cluster match.

 ReplicaSets should be used when your application is completely decoupled from the node and you can run multiple copies on a given node without special consideration. DaemonSets should be used when a single copy of your application must run on all or a subset of the nodes in the cluster.

An example of a case where you want a pod to run on each and every node in the cluster is when you want to run a resource monitor. Another good example is Kubernetes’ own kube-proxy process, which needs to run on all nodes to make services work. The diagram below illustrates how DaemonSets run only a single pod replica on each node, whereas ReplicaSets scatter them around the whole cluster randomly.

![daemonsets-ft-replicasets](https://github.com/ckodalo/daemonSet/assets/48943229/2f9ff6d7-d277-46b9-9a0d-4d81d55c03b2)
