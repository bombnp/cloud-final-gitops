# cloud-final-gitops

## To connect to GKE Autopilot cluster

1. Authenticate your gcloud sdk (your account must also have access to Google Cloud project)
2. run

```bash
$ gcloud container clusters get-credentials autopilot-cluster-1 --region asia-southeast1 --project cloud-final-346107
```

Your `kubectl` commands should now operate on the project cluster.

## Development

To access services for local development (such as database services), port-forward them to your local machine

InfluxDB

```bash
$ kubectl port-forward service/influxdb2 8086:8086
```

PostgreSQL

```bash
$ kubectl port-forward service/postgresql 5432:5432
```

You should now be able to access these services through the specified ports.
