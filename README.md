# nginx-app

## create a new namespace for the application
```
oc new-project nginx-app
```

&nbsp;


## create a new application using s2i
For this example we will be using the example nginx application that redhat provides
```
oc new-app centos/nginx-112-centos7~https://github.com/sclorg/nginx-ex --name nginx-sample-sapp
```
&nbsp;
## check if your pods are in running state
```
oc get pods
```
&nbsp;
## get the service name
```
oc get svc
````
 &nbsp;
## expose the route 
```
oc expose svc/nginx-sample-sapp
```
&nbsp;
## get the route and paster on your browser
```
oc get route
```
