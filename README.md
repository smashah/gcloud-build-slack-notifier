# Super Simple GCloud Build Slack Notifier

Slack integration for Google Cloud Build, using Google Cloud Functions to post messages to Slack.

## How

1. Clone the repo

1. Create a Slack app, and copy the webhook URL in index.js:
```
const SLACK_WEBHOOK_URL = "ENTER_WEBHOOK_URL_HERE";
```
2. Get deps
```
npm i
```
3. Deploy to google cloud functions (make sure you're using the right project by using gcloud init)
```
gcloud functions deploy subscribe --runtime nodejs8 --trigger-topic cloud-builds
```