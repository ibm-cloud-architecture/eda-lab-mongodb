go to docker-images/kafka-connector
build docker file
push it image repo

modify the image in kustomize/apps/base/kafka-connect/kafka-connect-cluster.yaml as below

image: us.icr.io/tvpt-rail-artifact/tvpt-kafka-connector:0.0.1

Note: add connectors to image as you needed. in this build camel file connector and mongodb connector included.

secrets and config need to be populated under overlays (preprod / prod)

Note: use jks files for certs.

