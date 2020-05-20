# wp-mariadb-yaml

YAML Template file for Wordpress with MariaDB deployment. While there have been many others wordpress deployment, most of them seperate the service, persistent volume, persistent volume claim and the container yaml files. This template yaml combine all these previously seperate file, and allow serivce, PV, PVC and container deployment in one yaml file. Keep in mind that this yaml doesn't contain route.

To deploy the template file, just use this command (on OpenShift, at least)

oc process -f template.yaml | oc apply -f-

This configuration/template deployment has been tested in RedHat Openshift with SE Linux Permissive and "oc adm policy add-scc-to-user anyuid -z default" setting applied to allow apache run in port 80. It should work on regular Kubernetes deployment.
