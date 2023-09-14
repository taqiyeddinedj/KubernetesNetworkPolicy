# CREATING DAEMONSET AND LIMITING IT
## Adding Labels to Nodes
The first step in limiting DaemonSets to specific nodes is to add the desired set of
labels to a subset of nodes. This can be achieved using the kubectl label command.

``` k label nodes k8snode ssd="true" ```

```touk@k8smaster:~$ k get nodes --selector ssd="true"
NAME      STATUS   ROLES    AGE   VERSION
k8snode   Ready    <none>   27d   v1.27.1
```
This will tweak the daemonset contrller workflow so it will create pods only nodes with a specifi label ssd="true"
### Unlable the nodes using hyphen at the end

```k label nodes k8snode ssd-```
