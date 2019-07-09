# Cognito-Intro
Users sign up and then sign in using userpool. Once they sign in they recieve a token. This token is then used to get Identity token which in turns are used to access aws services.

sign up to client using cli: this will automatically create the user 
aws cognito-idp sign-up --region us-east-1 --client-id < > --username <> --password <> --user-attributes Name=email value=<@gmail.com>

to sign up and confirmation:
aws cognito-idp admin-confirm-sign-up --region us-east-1 --user-pool-id <> --username <>
