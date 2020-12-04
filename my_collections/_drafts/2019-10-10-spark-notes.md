---
layout: post
title:  survival guide to spark
---
Spark is an analytics Operating System.

How to think in Spark - Ingest, Transform, Save

Ingest: 
t0 - Application AKA Driver connects with master 
t1 - Driver gets SparkSession
t2 - Master relies on Workers & their memory Partitions. A partition is a dedicated area in the worker’s memory.
t3 - Workers create Tasks & assigns a Partition to each task

Transform:
t4 - Spark Lazily notes down all Transformations kinda like a recipe

Save:
t5 - All worker nodes pushes data in it's partition into some form of DB
t6 - Control returns to Application

- no data has ever been transferred from the worker to the application.



Dataframe - Spark's internal data storage
