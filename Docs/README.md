# Udagram

  - [Description](#description)
    - [Infrastructure](#infrastructure)
    - [App dependencies](#app-dependencies)
    - [Environment Variables](#environment-variables)
  - [Pipeline Process](#pipeline-process)
  - [CircleCi](#circleci)

---

## Description
Udacity's advanced web nanodegree hosting a full stack application



### Infrastructure

- RDS - Database Host: database-1.ciijmq924rdm.us-east-1.rds.amazonaws.com
- RDS - Database Port: 5432
- RDS - Database Name: database-1
- S3 Endpoint - Frontend: http://udagrambucket.s3-website.us-east-2.amazonaws.com
- Elastic Beanstalk Endpoint - Backend: http://udagram-app-api-dev.eba-cj2mnmpz.us-east-1.elasticbeanstalk.com
- CircleCI



### App dependencies
```
- Node v16.15.0 (LTS)
- npm
- AWS CLI
- AWS EB CLI
- AWS RDS database running Postgres.
- AWS S3 bucket for Frontend.
- AWS Elastic Beanstalk for Backend.
- Angular
- Express
```

## Environment Variables

Setup the following variables in the .env file or in the cloud environments:
```
- AWS_BUCKET          
- AWS_REGION 
- JWT_SECRET     
- DB_PORT 
- POSTGRES_DB         
- POSTGRES_HOST  
- POSTGRES_PASSWORD  
- POSTGRES_USERNAME    
```

## Pipeline Process
- `npm run frontend:install`    - Install Front-End Dependencies
- `npm run api:install`         - Install API Dependencies
- `npm run frontend:build`      - Front-End Build Script
- `npm run api:build`           - API Build
- `sudo apt-get -y -qq update && sudo apt-get install python3-pip python3-dev build-essential && sudo pip3 install awsebcli && sudo pip3 install awscli` - Installing Deployment Dependencies
- `npm run ebPass`              - Send Environment Variables To EB
- `npm run api:deploy`          - API Deploy
- `npm run frontend:deploy`     - Frontend Deploy


## CircleCi
1. Install Front-End Dependencies
2. Install API Dependencies
3. Front-End Build Script
4. API Build
5. Installing Deployment Dependencies
6. Send Environment Variables To EB
7. API Deploy
8. Frontend Deploy


