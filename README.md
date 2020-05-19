# wp-mariadb-yaml
YAML Template file for Wordpress with MariaDB deployment. To expose the app, keep in mind you need to expose the route.

To deploy the template file, just use this command

oc process -f template.yaml | oc apply -f-

This configuration/template deployment has been tested in RedHat Openshift with SE Linux Permissive and "oc adm policy add-scc-to-user anyuid -z default" setting applied to allow apache run in port 80. It should work on regular K8s deployment.
