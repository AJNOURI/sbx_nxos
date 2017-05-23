# DevNet Open NX-OS Sandbox

Here you will find Sample Code, Scripts and Information for use in the DevNet [Open NX-OS Sandbox]().  

![](readme_images/sbx-nxos-base-topology.png)

[DevNet Sandboxes](http://developer.cisco.com/sandbox) are all about providing an environment where developers can explore and test out whatever they are learning or working on.  But sometimes having a starting point, or inspiration can be helpful, and that's what this repository is all about.  

And should you develop some interesting code targeting the Sandbox and want to share with the community, we'd love to include it here!!! Just fork the repo and review our [Pull Request instructions](pull-requests.md).  

# Repo Resources 

## Sandbox Management

This DevNet Sandbox leverages VIRL for building and managing the environment, however there is no need for you as the user to be familiar with VIRL to leverage the Sandbox resources.  

Should you run into issues with one or more of the nodes in the sandbox, or simply wish to restart the full environment, the following scripts are available to use within the [sbx-mgmt](sbx-mgmt) folder. 

* [status-sbx.py](sbx-mgmt/status-sbx.py): Check the status of the devices in the simulation.  A status of **ACTIVE** indicates a node that is booted.  
* [restart-sbx.py](sbx-mgmt/restart-sbx.py): Stop all the nodes in the simulation, and restart them.  The restart of the nodes takes about 2 minutes, but the Nexus 9000v's can take up to 15 minutes to fully boot.  

### Using the Scripts 

Before you can run the scripts, you need to have the `requests` Python module installed.  You can install it with `pip install requests`, or for convenience a [`requirements.txt`](sbx-mgmt/requirements.txt) file is included in the `sbx-mgmt` directory.  

```bash
# from the sbx_nxos directory and virtual env

pip install -r sbx-mgmt/requirements.txt 
```

Now you can execute the scripts like this: 

```bash
# from the sbx_nxos directory and virtual env
cd sbx-mgmt

# Check Status
python status-sbx.py

# Sample output
VIRL Simulation Name: nxos_9k-34mbMF

~mgmt-lxc: Status ACTIVE
nx-osv9000-4: Status ACTIVE
nx-osv9000-1: Status ACTIVE
nx-osv9000-3: Status ACTIVE
nx-osv9000-2: Status ACTIVE
server-2: Status ACTIVE
server-1: Status ACTIVE

# Restart
python restart-sbx.py
```


## Ansible Playbooks

Ansible is a great technology for Configuration Management of the network, and we've provided some sample playbooks to take a look at.  Take a look at what's available here:  [ansible-playbooks/README.md](ansible-playbooks/README.md).  

## NX-API REST Examples

Interested in using NX-API?  Checkout samples here: [nx-api/README.md](nx-api/README.md)

*Coming Soon!!!*

## Standard Model Driven Programmability with YANG

Looking for details on YANG Data Models and using NETCONF, RESTCONF, or gRPC with NX-OS?  Checkout samples here: [yang/README.md](yang/README.md)

*Coming Soon!!!*

## Guest Shell Use Cases

Want to run Linux utilities and apps on your Nexus devices?  Checkout samples here: [guestshell/README.md](guestshell/README.md)

*Coming Soon!!!*

## Other Use Cases

Interested in what else is possible?  Checkout ideas here: [other/README.md](other/README.md)

*Coming Soon!!!*
