# k8s-training

An interactive Kubernetes troubleshooting training platform that helps you practice real-world debugging scenarios in your own cluster.

## 🎯 Features

- **Real-world scenarios** for hands-on practice
- **Isolated namespaces** for safe experimentation
- **Hints system** with instructor-controlled guidance
- **Compatible** with any Kubernetes cluster

## 📋 Prerequisites

- Access to a Kubernetes cluster ([kind Quick Start](https://kind.sigs.k8s.io/docs/user/quick-start/))
- `kubectl` configured with cluster access (`kubectl get nodes` should work)

## 🛠️ Installation

```bash
# Set variables (replace with your platform, e.g., linux_arm64, darwin_amd64)
export VERSION=0.1.0
export OS_ARCH=darwin_arm64

# Download and extract
curl -L https://github.com/mbtamuli/k8s-training/releases/download/v${VERSION}/k8s-training_${VERSION}_${OS_ARCH}.tar.gz | tar -xz

# Move to PATH
sudo mv k8s-training /usr/local/bin/
chmod +x /usr/local/bin/k8s-training
```

**Verify Installation:**

```bash
k8s-training --help
```

You should see the help output confirming successful installation.

## ⚙️ Configuration

The CLI accepts kubeconfig in priority order (higher priority overrides lower):

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

**Happy troubleshooting!** 🚢⚓
