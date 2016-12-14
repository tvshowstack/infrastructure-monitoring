# Infrastructure Monitoring

It's a monitoring solution based on [Prometheus] (collecting data) and [Grafana] 
(displaying metrics) for [Kubernetes] cluster.
 
It's prepared for Grafana dashboard "[Kubernetes cluster monitoring (via Prometheus)]"
that displays CPU, memory and disk usage for nodes, pods, containers and system services.

### Outputs

* Prometheus Web UI - `http://<node-ip>:30900`
* Grafana - `http://<node-ip>:30910`

### Login

**Prometheus:**

No authentication needed.

**Grafana:**

* User: `admin`
* Password: `admin`

### Setup

**Grafana:**

1. Add [new data source] and as a URL use `http://prometheus:9090`
2. [Import dashboard] either from a local saved file or paste Grafana.net dasborad url or id

[Prometheus]: https://prometheus.io/
[Grafana]: http://grafana.org/
[Kubernetes]: http://kubernetes.io/
[Kubernetes cluster monitoring (via Prometheus)]: https://grafana.net/dashboards/315
[new data source]: http://docs.grafana.org/datasources/prometheus/
[Import dashboard]: http://docs.grafana.org/reference/export_import/
