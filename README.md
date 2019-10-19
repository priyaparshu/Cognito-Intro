# AWS Cognito

AWS cognito is an authentication and authorization service from AWS It consists of two parts 
  1. User Pools 
  2. Federated Identity Pool

In this example I am creating AWS Cognito UserPool and AWS Cognito Identity Pool using serverless framework.

Users sign up first and then sign in using userpool. Once they sign in they recieve a token. This token is then used to get Identity token which in turns are used to access aws services.

I have created a API gateway "hello"  purely for testing purpose.

# cli cheatsheet

sign up to client using cli: this will automatically create the user 
aws cognito-idp sign-up --region us-east-1 --client-id < > --username <> --password <> --user-attributes Name=email value=<@gmail.com>

to sign up and confirmation:
aws cognito-idp admin-confirm-sign-up --region us-east-1 --user-pool-id <> --username <>


initiate-authentication
aws cognito-idp initiate-auth auth-flow USER-PASSWORD-AUTH client-id <> --auth-parameters  USERNAME=<>  PASSWORD+<>
you will get refresh id and bearer token
