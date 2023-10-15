# AWS SES with Spring-Boot 

--    Create SES Identity and verify it 

--    install AWS CLI or put credential file in home/.aws folder

-- IAM secreat access id and secraet access key can be get it by creating IAM user with IAM.png plolicy

## Requirements
* Java 8
* Apache Maven 3.5.0 or higher

## How to Run

- Clone the project
- add the aws region you are using to application.yml file
- add a sender email address in application.yml note that sender email address should be verified by the SES
- Build the project  
```
mvn clean install
```
- Run the application
```
java -jar target/ses-1.0.0-SNAPSHOT.jar
```

- Send Request

```sh
POST  http://localhost:8080/api/v1/email
{
  "email": "youremail@gmail.com",
  "body": "Simple SES testing"
}
```

### Reference Documentation
For further reference, please consider the following sections:

(Aws SES developer guide) https://docs.aws.amazon.com/ses/latest/DeveloperGuide/send-using-sdk-java.html

(Using aws credentials) https://docs.aws.amazon.com/sdk-for-java/v2/developer-guide/credentials.html



## May u need to install AWS CLI or need to put credential file in {user-home}/.aws/credential