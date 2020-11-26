# idc-kubernetes-microservices
This is a repo where is allocated yamls files configurations.
KUBERNETES PASO POR PASO.

1. login en registry:

sudo docker login http://dmcontainerregister.azurecr.io/
Usuario: dmcontainerregister 
Password: 4GrE+yIpFkJ7qO07gJ9yj4sfh8OpCI0d

2. Obtener imágenes de un contenedor privado:


kubectl create secret generic regcred --from-file=.dockerconfigjson=config.json --type=kubernetes.io/dockerconfigjson


3. Comandos de consulta:

kubectl cluster-info
kubectl get all
kubectl get nodes: Conocer estado
kubectl get pods
kubectl get deploy
kubectl get svc

-o wide: Añade información adicional de red y ubicación 
Ejemplo:
kubectl get pods -o wide

4. Comandos de administración:

kubectl get logs (pod)
kubectl apply -f (recurso.yaml)
kubectl rollout restart deploy (nombre_deploy)
kubectl get (nombre_recurso: pods, deploy, svc, etc) -l etiqueta=etiqueta
kubectl describe (nombre_recurso)
kubectl exec -it (nombre_pod) bash
kubectl delete (nombre_recurso: pods, deploy, svc, etc)




