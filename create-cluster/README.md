[comment]: # ( Copyright Contributors to the Open Cluster Management project )

# Create and import a cluster on AWS, AZURE, GCP or vSphere

The script [deploy.sh](./deploy.sh) uses the [applier](https://github.com/open-cluster-management/library-go/blob/master/docs/applier.md) to apply a number of yamls on the hub in order to create a cluster and then import it as a managed cluster.

1. Make this directory your current directory
2. Create a values.yaml based on [values-template.yaml](./values-template.yaml) by setting your cluster name and your options for the different addons.
3. Login on the hub `kubectl login...`
4. run `./deploy.sh`.

# deploy.sh options

```
deploy.sh [-i values.yaml] [-o output-file] [-d] [-v [0-99]] [-h]
-i: the path to the values.yaml, default values.yaml
-o: output-file: generate an output-file instead of applying
-d: When set the cluster will be destroyed
-v: verbose level
-h: this help
```
