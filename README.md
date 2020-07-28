# azure-spring-cloud-gateway

## Create Gateway Java Project 
```
curl https://start.spring.io/starter.tgz -d dependencies=cloud-gateway,cloud-eureka,cloud-config-client -d baseDir=gateway -d bootVersion=2.2.5.RELEASE | tar -xzvf -
```

##  Create Gateway App in Azure
```
az spring-cloud app create -n gateway --is-public true
```


## Compile the App
```
./mvnw clean package -DskipTests -Pcloud
```

## Deploy Jar to Azure 
```
az spring-cloud app deploy -n gateway --jar-path target/demo-0.0.1-SNAPSHOT.jar
```

## Troubleshoot Deployment
```
az spring-cloud app deploy -n gateway --jar-path target/demo-0.0.1-SNAPSHOT.jar
```
