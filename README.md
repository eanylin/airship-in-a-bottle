# Airship in a Bottle

Airship is a new name for the project, formerly known as UCP.  References to
'UCP' or 'Undercloud Platform' will be corrected in time.

Airship is a broad integration of several components
enabling an automated, resilient Kubernetes-based infrastructure for hosting
Helm-deployed containerized workloads.

To get started, run the following in a fresh VM.  This will deploy Airship and OSH:
```
sudo -i
mkdir -p /root/deploy && cd "$_"
git clone https://github.com/openstack/airship-in-a-bottle
cd /root/deploy/airship-in-a-bottle/manifests/dev_single_node
./airship-in-a-bottle.sh
```

## Components

### Shipyard

Platform orchestrator for initial deployment, platform updates, and server
redeployments

### Promenade

The bootstrapper for the Kubernetes control plane - both on an initial genesis node
to get a working Kubernetes cluster and for adding additional nodes to the existing
Kubernetes cluster.

### Armada

Provisioner for Helm charts. Provides the capability to override chart values.yaml
items.

### Drydock

The orchestrator for physical asset provisioning (e.g. server deployment).

### Deckhand

YAML design data manager.
