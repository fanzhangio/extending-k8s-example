# Sample Database CRD and Controller by native approach
This repository implements a simple custom resource `Database` and controller which scales mysql deployments by native approach.

This follows the same pattern as that of the [Kuberentes sample-controller](https://github.com/kubernetes/sample-controller).

## Define and implement the CRD
Codes are orgnized by group, version, kind hierarchy under `./pkg/apis/`

## Implement Controller
Client side codes from the scratch, which resides in `./pkg/client` for creating a Kubernetes client to interact with Database API.

Implement a versioned clientset. `./pkg/client/clientset/versioned`
Implement an Informer for caching object & handling events. `./pkg/client/informers`
Implement a reference to Indexer. `./pkg/client/listers`
