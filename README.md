# monokle-ingress
Ingress service for Monokle
##Description:

Monokle Ingress template 

Go to, "..." in the top right and select, "plugin manager"

just place the following URL in the URL field:

https://github.com/mchenetz/monokle-ingress

This is the template

```
apiVersion: networking.k8s.io/v1
kind: Ingress
metadata:
  name: [[forms[0].name]]
spec:
  ingressClassName: nginx
  rules:
  - host: [[forms[0].host]]
    http:
      paths:
      - backend:
          service:
            name: [[forms[0].service]]
            port:
             number: [[forms[0].port]]
        path: [[forms[0].path]]
        pathType: Prefix
 ```
 
