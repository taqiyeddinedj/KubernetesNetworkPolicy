# CREATE A SHARED STORAGE BETWEEN CONTAINERS
## Create a pod with two contanier

```kubectl apply -f pod.yml```

In th manifest file i have created two aline container nd you can notice that i have used the volumes property which will let me create a specific volume type {configMap, emptyDir, amazonEBS...}
* emptyDir: 
the volume of type emptyDir is used to provide a temporary space that is shared between containers in the pod and is mounted on /cache1 and /cache2 respectively.