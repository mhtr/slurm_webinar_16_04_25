# Deploy a Production Ready Kubernetes Cluster

![Kubernetes Logo](https://raw.githubusercontent.com/kubernetes-sigs/kubespray/master/docs/img/kubernetes-logo.png)

## How to use

1. Clone repo.
```bash
git clone https://github.com/mhtr/slurm_webinar_16_04_25.git
```
2. Prepare environment.
```bash
VENVDIR=kubespray-venv
KUBESPRAYDIR=slurm_webinar_16_04_25
python3 -m venv $VENVDIR
source $VENVDIR/bin/activate
cd $KUBESPRAYDIR
pip install -U -r requirements.txt
```
3. Check the inventory in `inventory/sample/inventory.ini` and change it if necessary.
4. Run playbook
```bash
ansible-playbook cluster.yml -i inventory/sample/inventory.ini --become
```