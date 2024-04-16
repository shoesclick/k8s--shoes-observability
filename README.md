# Monitoramento - Prometheus e Grafana

Para subir a stack de Monitoramento no kubernetes 
Acesse a raiz do repositorio e Execute:

```
kubectl create namespace monitoring

kubectl create -f prometheus/clusterRole.yaml
kubectl create -f prometheus/configMap.yaml
kubectl create -f prometheus/deployment.yaml 
kubectl create -f prometheus/service.yaml
kubectl create -f prometheus/namespace.yaml

kubectl apply -f kube-state-metrics/

kubectl create -f grafana/configMap.yaml
kubectl create -f grafana/deployment.yaml 
kubectl create -f grafana/service.yaml
kubectl create -f grafana/namespace.yaml
```

Depois acesse http://<ip-load-balancer>:3000/ (Grafana)

Usuario: admin

Senha: admin

Importe o dashboard do GrafanaLabs (https://grafana.com/grafana/dashboards/12740)

ID: 12740

ou copie o conteudo desse arquivo "k8s-grafana/grafana-dashboard-kubernetes.json"
e importe no grafana.



```  
