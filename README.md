# Setup

`npm install --save-dev aws-sdk`
`npm install --save serverless-dynamodb-local`

## Local Testing

Install and run a local instance of dynamodb:

```
sls dynamodb install
sls dynamodb start --migrate
```

## Add a new candidate

Edit `test/post-event-1.json` and change the body to enter your data, then:

`sls invoke local --function candidateSubmission --path test/post-event-1.json`

## List all candidates:

`sls invoke local --function listCandidates`

## Get a specific candidate:

 Replace `pathParameter.id` in `test/get-event-1.json` with the right uuid, then:

`sls invoke local --function candidateDetails --path test\get-event-1.json`  
