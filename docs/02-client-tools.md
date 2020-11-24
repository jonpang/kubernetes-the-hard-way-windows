# Installing the Client Tools

In this lab you will install the command line utilities required to complete this tutorial: [cfssl](https://github.com/cloudflare/cfssl), [cfssljson](https://github.com/cloudflare/cfssl), and [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl).


## Install CFSSL

The `cfssl` and `cfssljson` command line utilities will be used to provision a [PKI Infrastructure](https://en.wikipedia.org/wiki/Public_key_infrastructure) and generate TLS certificates.

Download and install `cfssl` and `cfssljson`:

### Windows

1. Install Go [https://golang.org/doc/install](https://golang.org/doc/install) 


2. Verify `Go` version  1.15.5 or higher is installed: 
```
go version
```
> output
```
go version go1.15.5 windows/amd64
```

### Verification

Verify `cfssl` and `cfssljson` version 1.4.1 or higher is installed:

```
cfssl version
```

> output

```
Version: 1.4.1
Runtime: go1.6
```

```
cfssljson --version
```
```
Version: 1.4.1
Runtime: go1.6
```

## Install kubectl

The `kubectl` command line utility is used to interact with the Kubernetes API Server. Download and install `kubectl` from the official release binaries:

### Windows

[Kubectl Install](https://kubernetes.io/docs/tasks/tools/install-kubectl/)

Alternatively if curl installed
```
curl -LO https://storage.googleapis.com/kubernetes-release/release/v1.19.0/bin/windows/amd64/kubectl.exe
```
Move kubectl to bin folder or desired location
```
%USERPROFILE%\bin or %path to kubectl%
```
Add bin folder or desired location to PATH
```
%USERPROFILE%\bin or %path to kubectl%
```


### Verification

Verify `kubectl` version 1.18.6 or higher is installed:

```
kubectl version --client
```

> output

```
Client Version: version.Info{Major:"1", Minor:"18", GitVersion:"v1.18.6", GitCommit:"dff82dc0de47299ab66c83c626e08b245ab19037", GitTreeState:"clean", BuildDate:"2020-07-15T16:58:53Z", GoVersion:"go1.13.9", Compiler:"gc", Platform:"linux/amd64"}
```

Next: [Provisioning Compute Resources](03-compute-resources.md)
