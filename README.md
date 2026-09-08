# AWS GPU Observability and Agent

A personal engineering lab for GPU observability, controlled failure injection,
and verified recovery. Development happens on macOS; NVIDIA hardware integration
and the complete deployment run on AWS Linux.

## Intended outcome

Run a controlled GPU workload, detect stalled progress, collect diagnostic
evidence, perform a bounded recovery, and verify useful work resumed.

| Technology | Responsibility |
| --- | --- |
| C++ | Controlled GPU workloads and diagnostic agent |
| NVIDIA DCGM Exporter | Standard supported GPU telemetry |
| Prometheus / Alertmanager | Metrics, alert evaluation, and routing |
| Grafana | GPU health, workload progress, and recovery dashboards |
| Go / Temporal | Durable diagnostic and recovery workflows |
| PostgreSQL | Temporal persistence |
| Kubernetes / EKS | GPU scheduling, container lifecycle, and service deployment |
| Terraform | Reproducible AWS infrastructure and teardown |
| AWS EC2 / ECR / S3 | GPU and CPU compute, images, and diagnostic reports |

The initial integrated lab uses one GPU node and one CPU node. It is not highly
available. Cloud sessions are temporary; retained storage is managed explicitly.
