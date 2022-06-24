# Configuration Samples

In this section, you can find some examples of configuration files to set up
your PostgreSQL `Cluster`.

!!! Important
    These are here for demonstration and experimentation
    purposes, and can be executed on a personal Kubernetes cluster with Minikube
    or Kind as described in the ["Quickstart"](quickstart.md).

* [`cluster-example.yaml`](samples/cluster-example.yaml):
   a basic example of `Cluster` that uses the default storage class.
* [`cluster-example-custom.yaml`](samples/cluster-example-custom.yaml):
   a basic example of `Cluster` that uses the default storage class and custom parameters for `postgresql.conf` and `pg_hba.conf` files.
* [`cluster-storage-class.yaml`](samples/cluster-storage-class.yaml):
   a basic example of `Cluster` that uses a specified storage class of `standard`.
* [`cluster-storage-class-with-backup.yaml`](samples/cluster-storage-class-with-backup.yaml):
   an example of `Cluster` with backups configured. **WARNING**: assumes there is
   underlying bucket storage available. The sample config is for AWS, please change
   to suit your setup.
* [`backup-example.yaml`](samples/backup-example.yaml):
   an example of a backup that runs against the previous `cluster-storage-class-with-backup.yaml` example. Assumes the `pg-backup`
   cluster is in healthy state.
* [`cluster-pvc-template.yaml`](samples/cluster-pvc-template.yaml):
   a basic example of `Cluster` that uses a persistent volume claim template.
* [`cluster-example-full.yaml`](samples/cluster-example-full.yaml):
   an example of `Cluster` that sets most of the available options.
* [`cluster-example-replica-streaming.yaml`](samples/cluster-example-replica-streaming.yaml):
   a replica cluster following `cluster-example`, usable in a different namespace.
* [`cluster-example-replica-from-backup.yaml`](samples/cluster-example-replica-from-backup.yaml):
   a replica cluster following a cluster with backup configured. Usable in
   a different namespace.

For a list of available options, please refer to the ["API Reference" page](api_reference.md).
