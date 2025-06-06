# k8s-training

An interactive Kubernetes troubleshooting training platform that helps you practice real-world debugging scenarios in your own cluster.

## 📋 Prerequisites

- Access to a Kubernetes cluster
- `kubectl` configured with cluster access
- [Releases page](https://github.com/mbtamuli/k8s-training/releases) contains instructions for downloading and installing the CLI tool.

### Configuration Options

The CLI accepts kubeconfig in priority order(higher priority overrides lower):
```bash
# Using kubeconfig flag
k8s-training scenario create volume-void --kubeconfig /path/to/kubeconfig

# Using environment variable
export KUBECONFIG=/path/to/kubeconfig
k8s-training scenario create volume-void

# Uses default ~/.kube/config if neither above is set
```

## 🚀 Quick Start

1. **List available scenarios:**
   ```bash
   k8s-training scenario list
   ```

2. **Get detailed scenario information:**
   ```bash
   k8s-training scenario describe volume-void
   ```

3. **Create a scenario:**
   ```bash
   k8s-training scenario create volume-void
   ```

4. **Check scenario status:**
   ```bash
   k8s-training scenario status volume-void
   ```

5. **Start troubleshooting and verify your solution:**
   ```bash
   k8s-training scenario verify volume-void
   ```

6. **Get hints when stuck (requires instructor code):**
   ```bash
   k8s-training scenario hints volume-void
   ```

7. **Clean up when finished:**
   ```bash
   k8s-training scenario delete volume-void
   ```

## 🎯 Features

- **Real-world scenarios** for hands-on practice
- **Isolated namespaces** for safe experimentation
- **Hints system** with instructor-controlled guidance
- **Compatible** with any Kubernetes cluster

**Happy troubleshooting!** 🚢⚓
