# Assignment-2.5

1.Hadoop and Hadoop cluster

Hadoop: 
Hadoop is an open source framework, that supports the processing of large data sets in a distributed computing environment. 
Hadoop consists of MapReduce, the Hadoop distributed file system (HDFS) and a number of related projects such as Apache Hive, HBase and Zookeeper. MapReduce and Hadoop distributed file system (HDFS) are the main component of Hadoop. 

Hadoop cluster:
Normally any set of loosely connected or tightly connected computers that work together as a single system is called Cluster. In simple words, a computer cluster used for Hadoop is called Hadoop Cluster. 

Hadoop cluster is a special type of computational cluster designed for storing and analyzing vast amount of unstructured data in a distributed computing environment. These clusters run on low cost commodity computers. 

2.Racks and racks arrangement:
A Node is simply a computer. This is typically non-enterprise, commodity hardware for nodes that contain data. Storage of Nodes is called as rack. A rack is a collection of 30 or 40 nodes that are physically stored close together and are all connected to the same network switch. Network bandwidth between any two nodes in rack is greater than bandwidth between two nodes on different racks.A Hadoop Cluster is a collection of racks.
Arrangement:
This issue assumes that HDFS runs on a cluster of computers with a tree hierarchical network topology. For example, a cluster may be consisted of many datacenters filled with racks of computers, as shown in the right figure, in which leaves represent computers and inner
nodes represent switches/routers. Bandwidth in/out of a subtree may be less than the total
bandwidth of machines within the subtree.
The block replica placement policy is intended to get a tradeoff between minimizing thewrite cost and maximizing data reliability and availability, and aggregate read bandwidth.When a new block is created, the first replica is placed on the local node, the second one
is placed at a different rack, the third one is on a different node at the local rack, and the rest are placed on random nodes with restrictions that no more than one replica is placed at one node and no more than two replicas are placed in the same rack when the number
of replicas is less than twice of its rack number. 
