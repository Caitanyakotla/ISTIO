
Canary Deployments using Istio  

kubectl get pods -n istio-system

kubectl apply -f helloworld.yaml

kubectl apply -f helloworld.yaml -l version=v1

kubectl apply -f helloworld.yaml -l version=v2

kubectl apply -f helloworld-gateway.yaml

export GATEWAY_URL=$INGRESS_HOST:$INGRESS_PORT

curl http://$GATEWAY_URL/hello

Check LoadBalancer IP address:
kubectl get services  --all-namespaces  | grep istio-ingressgateway
