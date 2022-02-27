# Let's Encrypt SSL Generator

Use this to generate your SSL files for Java Spring

## How to

### Follow these steps to generate your certificate

* Clone this repository: `git clone https://github.com/suchorski/ssl-generator`
* Go inside it: `cd ssl-generator`
* Build with Maven: `mvn package`
* Go inside target folder: `cd target`
* Run it: `sudo java -Dserver.port=80 -Dacme.enabled=true -Dacme.domain-name=<YOUR_DOMAIN_NAME> -Dacme.key-store-password=<PASSWORD> -Dacme.accept-terms-of-service=true -jar ssl-generator-1.0.0.jar`

### And then add these configuration to your application.properties

```
server.port=443
server.ssl.key-store=keystore.p12
server.ssl.key-store-password=<PASSWORD>
server.ssl.keyStoreType=PKCS12
```