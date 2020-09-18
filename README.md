# api-starter-pack
## Starter project to quickly create a new Mule 4 application in Anypoint Studio. This sample project can be used as a project template and can be customised based on your organization's standards and protocols.
### Extensible properties:
- mule.env=**local** - used to load environment-specific configuration properties.
- mule.key=**mypassword123456** - used as encryption key for secured configuration properties. It's recommended to change this in your actual project.
- mule.logger.level=**DEBUG** - used to set the minimum logging level for loggers.
- splunk.url, splunk.token - required when the Splunk appender is enabled. Splunk is an web-based logging tool.
- anypoint.env=**Sandbox** - anypoint environment where to deploy your application using the mule maven plugin.
- cloudhub.region=**ap-southeast-2** - this is the cloudhub region where you want to deploy your mule application.
- workers=**1** - number of cloudhub workers for your application
- workerType=**Micro** - this is the size of your cloudhub worker

The default keystore password for server-keystore.jks is **changeit**.

### Maven command to deploy this application:
mvn clean package deploy -Dmule.env=sandbox -Dmule.key=mypassword123456 -Dmule.logger.level=INFO -Danypoint.env=Sandbox -Dcloudhub.region=ap-southeast-2 -Dworkers=1 -DworkerType=MICRO -DmuleDeploy

In your maven settings.xml, make sure to add your Anypoint Platform credentials so that you can deploy to cloudhub in your own Anypoint Platform environment.
```
  <server>
    <id>anypoint</id>
    <username>username</username>
    <password>password</password>
  </server>
```

### To test this API, open the APIKit console on your web browser after deploying this Mule application:
https://localhost:8082/console/
