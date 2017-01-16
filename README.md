# Nomie Pro Alexa Skill
Track your life with Nomie Pro and the Amazon Alexa

## Dependencies

- An [AWS account](https://console.aws.amazon.com/console/home)
- A ($9.99) [Nomie Pro API Key](https://connect.nomie.io)

## Quick Start

1. Create an [AWS Lambda](https://console.aws.amazon.com/console/home) function
   using `alexa-nomie.py` as the code
   - You can follow the [official Amazon
     instructions](https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/docs/developing-an-alexa-skill-as-a-lambda-function)
     to give you a hand
   - You can use `test_event.json` as your test template
   - Consider extending the timeout beyond the default of 3 seconds (I raised mine to 10, which is likely excessive, but eliminated some sporadic errors e.g. [#1](https://github.com/n8henrie/alexa-wolfram-alpha/issues/1))
   - Put your Nomie API Key into an environment variable called "NOMIE_KEY" and also put your Alexa Skill Identifier in an environement variable called "SKILL_ID". For help view the [documentation](http://docs.aws.amazon.com/lambda/latest/dg/env_variables.html)
1. Create a new [Alexa
   Skill](https://developer.amazon.com/edw/home.html#/skill/create) using
   `intent_schema.json` and `sample_utterances.txt`
1. **Don't publish** the skill (because it uses your personal Nomie API Key), leave it in development mode
1. Test that it's working from the web interface during the creation of the
   skill
1. Test that it's working with your Echo
