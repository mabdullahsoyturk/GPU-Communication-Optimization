# Evaluating Modern GPU Interconnect: PCIe, NVLink, NV-SLI, NVSwitch and GPUDirect

Evaluates 6 GPU Interconnects:

* PCIe
* NVLink-V1
* NVLink-V2
* NVLink-SLI
* NVSwitch
* GPUDirect enabled InfiniBand

Evaluates on six high-end servers and HPC platforms:

* P100-DGX-1
* V100-DGX-1
* DGX-2
* SummitDev 
* Summit
* An SLI-linked system with two RTX-2080 GPUs.

Multi-GPU execution scales in two directions:

* Vertically scaling-up **in a single node**
* Horizontally scaling-out **across multiple nodes**

Problems:

* There are no mature multi-GPU parallel programming, execution and performance models, largely due to the limited knowledge on how modern GPUs are interconnected as well as their communication patterns.
* Traditionally, inter-GPU communication shares the same bus interconnect as CPU-GPU communication, such as PCIe. This situation recently changed due to the introduction of GPU-oriented interconnect such as NVLink, NV-SLI and NVSwitch. Their characteristics and impacts are unknown.

They measure:

* Raw startup latency
* Sustainable uni/bi-directional bandwidth
* Network topology, 
* Communication efficiency 
* Routing 
* NUMA effects

Under two communication patterns:

* Peer-to-Peer
* Collective