# Review Catcher

A tool that you can search places such as restaurant and tourist attraction from Google Map, and check the review summary produced by genAI.


## System Structure

![system_design](./SystemDesign.jpg)

## Lambda Functions

#### Summarize Reviews

`Get mission from AWS SQS` -><br>
`Get reviews of the place` -><br>`Store reviews into AWS DynamoDB` -><br>`Send prompt and reviews to AWS Bedrock to generate summary` -><br>`Store summary into AWS DynamoDB and update the status`

- Get Summary

`Get summary and reviews from AWS DynamoDB`
