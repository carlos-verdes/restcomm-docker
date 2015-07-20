# restcomm-docker
Extend base gvagenas/restcomm docker image to make easier to deploy a new application.


The problem with gvagenas/restcomm is that the jboss has some war files inside the deployments folder (in jboss), so if you map the deployments folder to install your application you loose the default apps.

This image configure a new deployments folder inside standalone.xml so the user could mount the image as bellow:
```
docker run -v /yourAppFolder:/apps nosolojava/restcomm
```


... instead of
```
docker run -v /yourAppFolder:/opt/Mobicents-Restcomm-JBoss-AS7/standalone/deployments gvagenas/restcomm
```
