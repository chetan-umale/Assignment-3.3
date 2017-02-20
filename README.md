Q1-List the components of Hadoop 2.x and explain them in detail.

answer:

Components of Hadoop are as follows:


1.HDFS:
The hadoop distributed file system handles the storage aspect in hadoop.HDFS stores files in the form of blocks like traditional file systems,but the block size is very large ie. 128 MB.The blocks are stored in contiguous memory locations which improves access time.

HDFS is divided into 2 sub-components:

1.1 Name Node:
Name Node is responsible for namespace operations like opening and closing files,renaming files and directories and also stores metadata. 

1.2 Data Node:
Data Node actually stores the blocks of files.It is responsible for creation,deletion and replication of blocks.

2.MapReduce:
MapReduce is a batch processing paradigm used in hadoop for processing data.
In Hadoop 2.x MapReduce has following components:

2.1Resource Manager is a Per-Cluster Level Component.
Resource Manager is again divided into two components:
2.1.1 Scheduler
2.1.2 Application Manager

2.1.1 Resource Manager’s Scheduler is :
Responsible to scheduler required resources to Applications (that is Per-Application Master).
It does only scheduling.
It does care about monitoring or tracking of those Applications.

2.1.2Application Master:

Application Master is a per-application level component. It is responsible for:
Managing assigned Application Life cycle.
It interacts with both Resource Manager’s Scheduler and Node Manager
It interacts with Scheduler to acquire required resources.
It interacts with Node Manager to execute assigned tasks and monitor those task’s status.

2.2Node Manager:

Node Manager is a Per-Node Level component.
It is responsible for:
Managing the life-cycle of the Container.
Monitoring each Container’s Resources utilization.

3. Container:

Each Master Node or Slave Node contains set of Containers. In this diagram, Main Node’s Name Node is not showing the Containers. However, it also contains a set of Containers.
Container is a portion of Memory in HDFS (Either Name Node or Data Node).
