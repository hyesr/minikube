# Volume
Example pvc + pod
La pvc chiede il volume alla storage class che crea un pv per rispondere alla richiesta
1. Storage Class
NAME                 PROVISIONER                RECLAIMPOLICY   VOLUMEBINDINGMODE   ALLOWVOLUMEEXPANSION   AGE
standard (default)   k8s.io/minikube-hostpath   Delete          Immediate           false                  53m

2. PV
NAME                                       CAPACITY   ACCESS MODES   RECLAIM POLICY   STATUS   CLAIM                 STORAGECLASS   REASON   AGE
pvc-9e482261-8d66-45af-9bfd-a10411d7fda6   1Gi        RWO            Delete           Bound    default/my-pv-claim   standard                38m

3. PVC
NAME          STATUS   VOLUME                                     CAPACITY   ACCESS MODES   STORAGECLASS   AGE
my-pv-claim   Bound    pvc-9e482261-8d66-45af-9bfd-a10411d7fda6   1Gi        RWO            standard       37m



## Configure a Pod to Use a PersistentVolume for Storage
Create an index.html file on your Node
Create a PersistentVolume
Create a PersistentVolumeClaim 
Create a Pod 