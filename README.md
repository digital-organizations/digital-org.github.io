# Digital Org Application

Circle CI   
[![Digital Org](https://circleci.com/gh/digital-organizations/digital-org.svg "CircleCI status")](https://circleci.com/gh/digital-organizations/digital-org)
[![Digital Org-UI](https://circleci.com/gh/digital-organizations/digital-org-ui.svg "CircleCI status")](https://circleci.com/gh/digital-organizations/digital-org-ui)

Travis    
[![Build Status](https://travis-ci.com/digital-organizations/digital-org.svg?token=uk63pxdAgoFGezW3mmw9&branch=master)](https://travis-ci.com/digital-organizations/digital-org)
[![Build Status](https://travis-ci.com/digital-organizations/digital-org-ui.svg?branch=master)](https://travis-ci.com/digital-organizations/digital-org-ui)

Note : Older builds are on [Circle CI](https://app.circleci.com/gh/digital-organizations/). Due to Codecov integration of migrated to Travis.

Codacy  
[![Codacy Badge](https://app.codacy.com/project/badge/Grade/a0080fc3dbe7469281991a52bfa02247)](https://www.codacy.com/gh/digital-organizations/digital-org/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=digital-organizations/digital-org&amp;utm_campaign=Badge_Grade)
[![Codacy Badge](https://app.codacy.com/project/badge/Grade/53084fdca1424bb9b0d3e8ec2bde57fc)](https://www.codacy.com/gh/digital-organizations/digital-org-ui/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=digital-organizations/digital-org-ui&amp;utm_campaign=Badge_Grade)

Codecov   
[![codecov](https://codecov.io/gh/digital-organizations/digital-org/branch/master/graph/badge.svg?token=2UCY3W0QLK)](https://codecov.io/gh/digital-organizations/digital-org)
[![codecov](https://codecov.io/gh/digital-organizations/digital-org-ui/branch/master/graph/badge.svg?token=2UCY3W0QLK)](https://codecov.io/gh/digital-organizations/digital-org-ui)

NPM  
[![npm version](https://badge.fury.io/js/%40angular%2Fcore.svg)](https://www.npmjs.com/@angular/core)
 
#### appUrl: [digital-organization](https://digital-organizations.github.io/digital-org.github.io/)
  
  
#### openApiUrl: [digital-organizations swagger-ui](https://digital-org.herokuapp.com/swagger-ui/#/)

#### monitoringUrl: 

[Kibana](https://da02d396d35a43068d3ae7f1114cae90.us-east-1.aws.found.io:9243)
username : elastic
password : [copy from this link](a0Ny8XFNvg7u1znkZeeaO3mR)

repositories: 

```    -
      name: digital-org
      githubUrl: https://github.com/digital-organizations/digital-org
      travisUrl: https://travis-ci.com/github/digital-organizations/digital-org
      circleUrl: https://app.circleci.com/pipelines/github/digital-organizations/digital-org
      codacyUrl: https://app.codacy.com/gh/digital-organizations/digital-org/dashboard
      coverageUrl: https://codecov.io/gh/digital-organizations/digital-org
```

```    
    - name: digital-org-ui
      githubUrl: https://github.com/digital-organizations/digital-org-ui
      travisUrl: https://travis-ci.com/github/digital-organizations/digital-org-ui
      circleUrl: https://app.circleci.com/pipelines/github/digital-organizations/digital-org-ui?branch=master
      codacyUrl: https://app.codacy.com/gh/digital-organizations/digital-org-ui/dashboard
      coverageUrl: https://codecov.io/gh/digital-organizations/digital-org-ui
```

####PostgreSQL schema(Hosted on AWS)
![digital](assets/images/digital.png)
  


## 1. How to start in local

Springboot : http://localhost:8080/swagger-ui/#/  (based on server.port)
```
$ git clone
$ cd digital-org
$ mvn spring-boot:run

```


###### Angular  : http://localhost:4200
```
$ git clone
$ cd digital-org-ui
$ npm install
$ ng serve

```

###### Heroku CLI :
```
$ heroku login
$ heroku apps
$ heroku logs -t --app digital-org
```

###### Monitoring 
```
Elastic  : https://c013054f3b784fcfa1caa48efc9d0f18.us-east-1.aws.found.io:9243
Kibana   : https://da02d396d35a43068d3ae7f1114cae90.us-east-1.aws.found.io:9243
username : elastic
password : a0Ny8XFNvg7u1znkZeeaO3mR
```

##### APM Configuration
```
java -javaagent:/Downloads/elastic-apm-agent-1.18.0.jar -Delastic.apm.service_name=digital-org -Delastic.apm.server_urls=https://fa91e1be347d4b319d59967c6d5d6b0e.apm.us-east-1.aws.cloud.es.io:443 -Delastic.apm.secret_token=gf5vlw7rzG1I01MAKv -Delastic.apm.application_packages=com.engg.digitalorg -jar digital-org-0.0.1-SNAPSHOT.jar
```


