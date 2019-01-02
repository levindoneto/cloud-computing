# WEEK 01 - CLOUD COMPUTING CONCEPTS

## Cloud

It pretty much relates to distributed systems -> cluster -> collection of machines.

### Features

* Massive scale.
* On-demand nature.
* Data-intensive nature.
* New cloud programming paradigms (Hadoop, map-reduce).

## Distributed System

It is a collection of entities, each of which is:

* Autonomous.
* Programmable.
* Async.
* Failure prone.

and which communicate through an unreliable communication medium.

## Map Reduce

Using as an example a counter of words in the following sentence:

```
welcome everyone hello everyone
```

### Map tasks

| Key      | Value  |
| -------- |:------:|
| welcome  | 1      |
| everyone | 1      |
| hello    | 1      |
| everyone | 1      |

Map tasks may be processed in parallel.

### Reduce tasks

Here it is where the pairs with the same key are merged.

| Key      | Value  |
| -------- |:------:|
| everyone | 2      |
| hello    | 1      |
| welcome  | 1      |

`key 1<->1 reduce`

## Map Reduce Scheduling

No reduce tasks can start before all the map tasks are done (barrier).

### YARN Scheduller

* Used in Hadoop 2.x+.
* Treats each server as a collection of containers.

#### Main Components

* Global Resource Manager.
* Pre-Server Node Manager (daemon and server-specific functions).
* Per-Application (job) Application Master.

More information may be found [here](https://www.slideshare.net/martyhall/hadoop-tutorial-mapreduce-part-6-job-execution-on-yarn).

## Map Reduce Fault-Tolerance

TODO.

## Homework

It may be found in the folder [homework](homework/).
