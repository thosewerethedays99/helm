Blackbox exporter Helm chart for kube-prometheus-stack

#Implementation

1.Install Blackbox exporter chart with Helm 3
```
	helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
	helm repo update
	helm -n monitoring install prometheus-blackbox-exporter prometheus-community/prometheus-blackbox-exporter -f kube-prometheus-stack-blackbox-exporter-custom-values.yaml
```

2.Install kube-prometheus-stack with custom values
```
helm -n monitoring install monitor-didi-test prometheus-community/kube-prometheus-stack -f blackbox-exporter-custom-values.yaml
```