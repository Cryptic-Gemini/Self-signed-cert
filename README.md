# Self-signed-cert
                                   
                                   Assignment for Configmap and secrets

Task:
----

Run nginx web-server, which listens on port 443, by using some self-signed SSL certificates. This involves:

a- providing SSL certificates to nginx pods, and,

b-providing a custom nginx configuration, so the pods know how to use these certificates and what port to listen on.


Help:
-----

To achieve these objectives, we will create SSL certs as secrets, and a custom nginx configuration as configmap, and use them in our deployment.

1- Generate self signed certs: (check support-files/ directory in https://github.com/KamranAzeem/kubernetes-katas.git)

                 ./generate-self-signed-certs.sh

This will create tls.* files.

2- Create (tls type) secret for nginx.

3- Create a custom configuration for nginx.

4- Create a nginx deployment with SSL support using the secret and config map you created in the previous steps.

5- Expose it as a service of type NodePort

 You will get two NodePorts as  443:31754/TCP,80:30925/TCP


6- You should be able to see nginx running on browser through http and https.
