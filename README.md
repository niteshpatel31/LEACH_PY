# LEACH-PY

### Low-energy adaptive clustering hierarchy

Low-energy adaptive clustering hierarchy ("LEACH") is a TDMA-based MAC protocol that is integrated with clustering and a simple routing protocol in wireless sensor networks (WSNs). LEACH aims to lower the energy consumption required to create and maintain clusters to improve the lifetime of a wireless sensor network. 

LEACH is a hierarchical protocol in which most nodes transmit to cluster heads, and the cluster heads aggregate and compress the data and forward it to the base station (sink). Each node uses a stochastic algorithm at each round to determine whether it will become a cluster head in this round. LEACH assumes that each node has a radio powerful enough to reach the base station or the nearest cluster head directly, but that using this radio at full power all the time would waste energy.

Nodes that have been cluster heads cannot become cluster heads again for P rounds, where P is the desired percentage of cluster heads. Each node has a 1/P probability of becoming a cluster head again. At the end of each round, each node that is not a cluster head selects the closest cluster head and joins that cluster. The cluster head then creates a schedule for each node in its cluster to transmit its data.

All nodes that are not cluster heads only communicate with the cluster head in a TDMA fashion, according to the schedule created by the cluster head. They do so using the minimum energy needed to reach the cluster head, and only need to keep their radios on during their time slot.

LEACH also uses CDMA so that each cluster uses a different set of CDMA codes, to minimize interference between clusters. 

### Properties

Properties of this algorithm include:

* Cluster based
* Random cluster head selection for each round with rotation. Or cluster head selection based on the sensor having the highest energy
* Cluster membership adaptive
* Data aggregation at cluster head
* Cluster head communicates directly with sink or user
* Communication is done with the cluster head via TDMA
* Threshold value


### Shortcomings of LEACH

Shortcomings of LEACH include:

- Remaining energy among the nodes isn't considered when selecting Cluster Heads
- Random and variable size cluster formations
- Random and uneven distribution of cluster heads
- Single-hop communication in situations where energy use is less efficient from cluster head to base station

# Run Code
### Clone this repository 
```bash 
git clone https://github.com/niteshpatel31/LEACH_PY.git leach
```
### Change directory to leach
```bash
cd leach
```
### Create Python Virtual Environment (venv)
```bash
python -m venv env
```
### Activate Environment
```bash
source env/vin/activate
```
### Install all python packages using pip
```bash
pip install -r requirements.txt
```
### Start python program
```bash
python leach.py
```

# Video Guide
https://github.com/niteshpatel31/LEACH_PY/assets/150846500/ecc3ecab-e0da-45fb-b95c-1201c8cbfa1b

---

This code was originally written by Hritwik Singhal and Nishita Agarwal and was based on the Matlab code of Amin-Nazari.

---

This code is licensed under GPLv3.
