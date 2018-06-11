# serverless

Simple hello world exercise with serverless

Steps:

1. Lets install the serverless globally 

`npm install -g serverless`

2. Lets connect the communication between serverless code and aws.

- create the IM user in aws console 
- give it a programmatic access 
- save the access details having access key and secrets

3. Run the following command
` serverless config credentials --provider aws --key xxxxxxxxxxxxxx --secret xxxxxxxxxxxxxx`

4. create the service using template
`serverless create --template aws-nodejs --path my-service`

5. edit he serverless.yml to support the event

6. deploy the code 
`serverless deploy -v`

7. Test from command prompt
`serverless invoke -f hello -l`

8. To run locally and deploy as we edit, we need serverless-offline npm module
`npm init`
`npm install serverless-offline --save-dev`

9. Edit the serverless.yml and add the plugin details

```# adding these two lines
plugins:
  - serverless-offline```

 10. Run it locally
 `serverless offline start`

 11. Launch http://localhost:3000/hello/get
