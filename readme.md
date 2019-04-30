# Helm chart to install Velero server components in the VMware PKS Ninja lab environment.

Note: Due to limitations of cleaning up CRDs in current Helm versions, you will need to manually delete the CRDs created by this installation before installing the chart again. If you need to re-install the chart, you can download the /pksNinjaVelero/templates/00-prereqs.yaml file and run `kubectl delete -f 00-prereqs.yaml` to delete the CRDs from the cluster.

Minio S3 appliance is installed and exposed via ingress at http://minio.ing.corp.local with username admin and password VMware1!

You will need to download and untar the client-side CLI tool from the Velero repo. Intro to Velero lab guide has directions for this.

#### Directions: Once you have a cluster deployed and have configured Helm (see Intro to Helm lab guide), execute the following:
```
 helm install https://raw.githubusercontent.com/natereid72/pksNinjaVeleroHelmChart/master/pksNinjaVelero-1.0.0.tgz
 ```
