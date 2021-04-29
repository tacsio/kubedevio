# kubedevio

### Components
- Pod (container runtime)
- ReplicaSet (resilience and scalability manager)
- Deployment (manages version updates)

> Quanto trabalhamos com replicasets não é necessário definir o pod separado, ele já é definido na própria construção do replicaset.

> Quando trabalhamos com deployments não é necessário definir o replica set, ele já é definido na própria construção do deployment, assim como o pod.

### Create Components
```
kubectl apply -f [file.yml]
```

#Delete componentes
kubectl delete -f [file.yml]

### Port forward (cmd)
```
kubectl port-forward pod/[podname] [host_port:container_port]
```

### Scale replica set (cmd)
```
kubectl scale replicaset [replica set name] --replicas [number of replicas]
```

> Ao atualizar o replica set com uma nova versão da imagem do container, apenas novos pods são criados com a versão nova definda.

### Service
- ClusterIP (expose pod internally)
- NodePort (expose externally through any node's ip of cluster)
- LoadBalance (integrates with cloud service to define external ip to acces the service)


### Info
```
kubectl get pods -o wide
```

### Rollout
```
kubectl rollout undo deployment meudeployment 
```
