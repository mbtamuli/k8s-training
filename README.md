# k8s-training

An interactive Kubernetes troubleshooting training platform that helps you practice real-world debugging scenarios in your own cluster.

## 🚀 Quick Start

1. **Install** from [Releases](https://github.com/mbtamuli/k8s-training/releases) - contains download and installation instructions for all platforms

1. **Verify** installation:
   ```bash
   k8s-training --help
   ```

1. **Start** practicing:
   ```bash
   # List available scenarios
   k8s-training scenario list
   
   # Create a scenario
   k8s-training scenario create volume-void
   
   # Start troubleshooting!
   kubectl get pods -n k8s-training-volume-void
   
   # Verify your solution
   k8s-training scenario verify volume-void
   ```

## 📋 Prerequisites

- Access to a Kubernetes cluster
- `kubectl` configured with cluster access

## 🎯 Features

- **Real-world scenarios** for hands-on practice
- **Isolated namespaces** for safe experimentation
- **Hints system** with instructor-controlled guidance
- **Compatible** with any Kubernetes cluster

**Happy troubleshooting!** 🚢⚓
