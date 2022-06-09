# CouchDB-Cluster-formation-in-AWS-using-ECS
AWS architecture for automatic couchdb cluster formation workflow

Creating a CouchDB cluster involves many manual steps which are very tedious to perform
on a large-scale cluster. To make it a bit more convenient I constructed an AWS architecture
that allows us to form a CouchDB cluster with minimal manual configuration.

This AWS architecture uses services like Amazon Elastic Container Services, Elastic Container
Registry, EC2, CloudTrail, S3, Lambda function, and Relational Database Services MySQL.

For the cluster node, we are going to use the CouchDB docker container which will be
hosted in the EC2 instance. For forming a CouchDB cluster it is necessary that the cluster
nodes can communicate with each other, and each node should have a unique NODENAME
in the cluster. To avoid any name clash it is advisable to use the private Ip of the host
instance in the NODENAME so that it will always be unique among all the cluster nodes.

<img alt="png" src="https://github.com/sahilkhatri/CouchDB-Cluster-formation-in-AWS-using-ECS/blob/main/ECS.png">

<img alt="png" src="https://github.com/sahilkhatri/CouchDB-Cluster-formation-in-AWS-using-ECS/blob/main/ClusterFormation.png">
