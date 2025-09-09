
# enable-cim-helm

A Helm chart to configure the **Multi‑Cluster‑Engine (MCE)** and enable **Central Infrastructure Management (CIM)**.

---

## Overview

This Helm chart helps streamline and automate enabling CIM capabilities via MCE in OpenShift clusters. It encapsulates the necessary `ConfigMap`, values, and template logic to simplify deployment, especially in multi-cluster management scenarios.

---

## Contents

- **Chart.yaml** – Metadata for the Helm chart (name, version, etc.).
- **values.yaml** – Default configuration values; override as needed.
- **configmap.yaml** – Defines the core config used by MCE to enable CIM.
- **templates/** – Template files that render Kubernetes resources based on `values.yaml`.

---

## Prerequisites

- A Kubernetes or OpenShift cluster (MCE-compatible).
- **Multi‑Cluster‑Engine (MCE)** installed and functional.
- Helm 3.x installed locally and configured to communicate with your cluster.

---

## Installation

1. Add your chart repository or use a local path:
   ```bash
   helm repo add my‑repo <your-chart-repo-url>
   helm repo update
````

2. Install with default settings:

   ```bash
   helm install enable-cim my‑repo/enable-cim-helm
   ```

3. To customize settings:

   ```bash
   helm install enable‑cim my‑repo/enable‑cim‑helm \
     --values custom-values.yaml
   ```


## Uninstallation

To clean up the deployed resources:

```bash
helm uninstall enable-cim
```

This removes the ConfigMap and any related resources created by the chart.

```

---

## Contributing

Contributions are welcome! To help improve the chart:

* Open issues to report bugs or request enhancements.
* Submit pull requests for fixes or new features.

---

## License

Apache-2.0 

---

