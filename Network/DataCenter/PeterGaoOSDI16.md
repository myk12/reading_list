# Network Requirements for Resource Disaggregation

## Basic Info

**Source**: https://www.usenix.org/system/files/conference/osdi16/osdi16-gao.pdf

***Year**:  2016*

**Publisher**: OSDI

**Theme**: *Disaggregated Memory*, *Data Center*, *Measurement*

**Abstract**:

> Traditional datacenters are designed as a collection of servers, each of which tightly couples the resources required for computing tasks. Recent industry trends suggest a paradigm shift to a disaggregated datacenter (DDC) architecture containing a pool of resources, each built as a standalone resource blade and interconnected using a network fabric. A key enabling (or blocking) factor for disaggregation will be the network – to support good application-level performance it becomes critical that the network fabric provide low latency communication even under the increased traffic load that disaggregation introduces. In this paper, we use a workload-driven approach to derive the minimum latency and bandwidth requirements that the network in disaggregated datacenters must provide to avoid degrading application-level performance and explore the feasibility of meeting these requirements with existing system designs and commodity networking technology.

## Brief Summary

In order to find out the network requirments (bandwidth, latency, et al.) of realizing Disaggregated Data Center, the paper conduct a series of emulation and simulation. The results show that the bandwidth requirement of 40~100Gbps is already realized by the current data center fabric. However the latency requirment of 3 ~ 5 microseconds is hard to achieve. One optimzation direction is using RMDA or NIC integration in order to eliminate the kernel execution time which account for half of the latency.

## Detailed Summary

**Topic**:

The paper is related to the design and requirements of network architectures for disaggregated datacenters (DDCs). ^^ In DDCs, resources like CPUs, memory, and storage are separated into standalone "blades" and interconnected by a network fabric, rather than being tightly coupled within traditional servers.

**Goals**:

* The paper aims to evaluate the minimum network requirements (latency and bandwidth) to support resource disaggregation without significantly degrading application performance.
* It also explores the feasibility of meeting these requirements using existing networking technology.

**Challenges:**

* Disaggregating resources increases network traffic as inter-resource communication that was previously within a server now traverses the network.
* Ensuring low-latency communication becomes critical to maintain application performance.

**Meathods**:

* They use a workload-driven approach, evaluating network requirements in the context of ten workloads from seven open-source systems.
* They use emulation, simulation, and implementation to derive the minimum latency and bandwidth requirements.
* They analyze the impact of network latency and bandwidth on application-level performance.

**Comparison**:

* The paper argues that previous work relies heavily on specialized network hardware and architectures without thoroughly evaluating the potential of existing commodity networking technology.
* Their evaluation provides a quantitative analysis of network requirements for DDCs, which was lacking in prior research.
* They demonstrate that in certain scenarios, disaggregation is feasible with existing network hardware and transport protocols.

**contributions**:

* Network bandwidth in the range of 40-100Gbps is sufficient for disaggregation.
* Network latency in the range of 3-5µs is crucial for maintaining application performance.
* Network software overhead is a significant bottleneck.
* For some applications, disaggregation at the datacenter scale is feasible.
* Existing transport protocols (TCP, DCTCP) may not be optimal for DDCs, and research proposals like pFabric and pHost show promise.
