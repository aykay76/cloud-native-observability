
Download fluentd image from: docker pull fluent/fluentd:edge

docker swarm init
docker stack deploy --compose-file docker-compose.yml bob

docker events : to see what's happening!
docker stats  : to see what's happening

docker service ls : to get a list of services
docker service log <first 3 id chars> : to see what's happening inside the container

use <stack>_<service> as host name for connectivity:
e.g. in Grafana add http://prometheus:9090/ as source



kubectl create configmap fluent-cm --from-file fluentd/fluentd.conf
kubectl create configmap prometheus-cm --from-file prometheus/prometheus.yml
kubectl apply -f p.yml
kubectl apply -f g.yml
