# ISTIO

************Canary Deployments using Istio**************************

# Also ensure corresponding Kubernetes pods are deployed and have a STATUS of Running:
# kubectl get pods -n istio-system

Also ensure corresponding Kubernetes pods are deployed and have a STATUS of Running:
kubectl get pods -n istio-system


kubectl apply -f helloworld.yaml
kubectl apply -f helloworld.yaml -l version=v1
kubectl apply -f helloworld.yaml -l version=v2

kubectl apply -f helloworld-gateway.yaml


export GATEWAY_URL=$INGRESS_HOST:$INGRESS_PORT
curl http://$GATEWAY_URL/hello



Check LoadBalancer IP address:
kubectl get services  --all-namespaces  | grep istio-ingressgateway
