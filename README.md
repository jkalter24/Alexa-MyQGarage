# Alexa-MyQGarage
Using the Alexa Skills Kit to control your Chamberlain MyQ garage door.

## Description
By using the Alexa Skills Kit and AWS Lambda, you can control your Chamberlain MyQ garage door through your Amazon Echo.
This code adapts [David Pfeffer's](https://github.com/pfeffed) unofficial [Chamberlain Liftmaster API](http://docs.unofficialliftmastermyq.apiary.io/) to a Python-based app you can use inside of AWS Lambda.

## Usage
1. Create an Alexa Skills Kit (ASK) app, using the intent schema, custom slot values, and sample utterances in this repo. Choose an invocation name like `my garage door`.
2. Replace `<MYQ_LOGIN_USERNAME>` and `<MYQ_LOGIN_PASSWORD>` in `main.py` with the username and password you created at Chamberlain, and substitute `amzn1.echo-sdk-ams.app.<your-alexa-skills-id>` with the ID of the ASK skill you created. The `APP_ID` should remain the same, it is Chamberlain specific and not specific to your MyQ account.
3. Zip of the contents of this repo and upload as a new [AWS Lambda](https://console.aws.amazon.com/lambda/home) function, and add "Alexa Skills Kit" as an "Event Source".
4. Modify your ASK skill with the [ARN](http://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) of your newly created function.
5. Test your interactions with the ASK console. When you've got it working, try it on your Echo: `Alexa, ask my garage door to open`.

## Alexa Skills Kit Documentation
The documentation for the Alexa Skills Kit is available on the [Amazon Apps and Services Developer Portal](https://developer.amazon.com/appsandservices/solutions/alexa/alexa-skills-kit/).

## Resources
Here are a few direct links to Alexa and Lambda documentation:

- [Using the Alexa Skills Kit Samples (Node.js)](https://github.com/amzn/alexa-skills-kit-js)
- [Getting Started](https://developer.amazon.com/appsandservices/solutions/alexa/alexa-skills-kit/getting-started-guide)
- [Invocation Name Guidelines](https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/docs/choosing-the-invocation-name-for-an-alexa-skill)
- [Developing an Alexa Skill as an AWS Lambda Function](https://developer.amazon.com/appsandservices/solutions/alexa/alexa-skills-kit/docs/developing-an-alexa-skill-as-a-lambda-function)

### Disclaimer

The code here is based off of an unsupported API from [Chamberlain](http://www.chamberlain.com/) and is subject to change without notice. The authors claim no responsibility for damages to your garage door or property by use of the code within.
