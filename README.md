# NATS Streaming Server on Kubernetes for event-bus for catalogue

This project contains a Helm chart to run NATS Streaming Server in the Kubernetes cluster and `.gitlab-ci.yaml` file for manual deployment on stage and production.
Currently supports only file store.


## Manual deploy (for testing purposes)
```
helm upgrade --tiller-namespace="FILL-SOMETHING" --namespace="FILL-SOMETHING" --install --wait --timeout 60 --set environment.name="FILL-SOMETHING" --values ./charts/nats-streaming/values.yaml --kube-context "FILL-SOMETHING"  "FILL-SOMETHING" ./charts/nats-streaming
```

## TODO
- add support for mysql
- try nats streaming operator https://github.com/nats-io/nats-streaming-operator