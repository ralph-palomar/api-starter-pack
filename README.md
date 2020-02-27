# api-starter-pack
## Starter project to quickly create a new Mule 4 application in Anypoint Studio. This sample project can be used as a project template and can be customised based on your organization's standards and protocols.
### Extensible properties:
- mule.env=**local** - used to load environment-specific configuration properties.
- mule.key=**mypassword123456** - used as encryption key for secured configuration properties. It's recommended to change this in your actual project.
- mule.logger.level=**DEBUG** - used to set the minimum logging level for loggers.
- splunk.url, splunk.token - required when the Splunk appender is enabled.
- cloudhub.env=**Sandbox** - cloudhub environment where to deploy your application using the mule maven plugin.

The default keystore password for server-keystore.jks is **changeit**.

### Maven command to deploy this application:
mvn clean package deploy -Dmule.env=sandbox -Dmule.key=mypassword123456 -Dmule.logger.level=INFO -Dcloudhub.env=Sandbox -DmuleDeploy
