# ansible-role-grafana-agent
An agent to be deployed on every host we want to monitor. The default deployment mode of Grafana Agent is a drop-in replacement for `Prometheus remote_write`. Grafana Agent acts similarly to a `single-process Prometheus`, doing service discovery, scraping, and remote writing.

- promtail (embedded)
    - scrape systemd logs
    - scrape /var/log

- cadvisor (embedded)
    - gathers container metrics

- node_exporter (embedded)
    - gathers host (node) metrics

## Useful Docs
- [Grafana Agent - overview](https://grafana.com/docs/agent/latest/)
- [Grafana Agent - cadvisor configuration](https://grafana.com/docs/agent/latest/configuration/integrations/cadvisor-config/)
- [Grafana Agent - node_exporter configuration](https://grafana.com/docs/agent/latest/configuration/integrations/node-exporter-config/)
- [Practical (slightly outdated) Example with Docker Swarm](https://zeigren.com/posts/monitoring_prometheus_loki/)
- [Introduction of Prometheus "Agent" mode](https://prometheus.io/blog/2021/11/16/agent/)
- [Why Prometheus "Agent" was created _from_ Grafana Agent](https://grafana.com/blog/2021/11/16/why-we-created-a-prometheus-agent-mode-from-the-grafana-agent/)
- [My reddit post, "Prometheus Agent mode vs. Grafana Agent"](https://www.reddit.com/r/PrometheusMonitoring/comments/vxpnvd/prometheus_agent_mode_vs_grafanaagent/)

