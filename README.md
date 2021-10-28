# opensheet

A free API for getting Google Sheets as JSON.

**Documentation blog post:** [benborgers.com/posts/google-sheets-json](https://benborgers.com/posts/google-sheets-json)

## Self-hosting

If you host opensheet in your own Vercel account or make a fork, you’ll need to get your own Google Sheets API credentials:

1. Go to the [Google Cloud Console](https://console.cloud.google.com) and create a new project from the top navigation bar.
2. Search for “Google Sheets API” and enable it.
3. On the left bar, go to Credentials and click “Create Credentials” → “Service account”. _Service accounts_ are Google’s concept for a Google account that you can control programmatically.
4. Fill in any reasonable name, and skip the next two optional steps. Click “Done” to create the set of credentials, which will allow you to access Google Sheets using the API.
5. Click on this newly created service account, and then go to the “Keys” tab. Create a key of type JSON.
6. A JSON file containing the service account’s credentials will be downloaded. Open up that file, and copy its entire contents. This is similar to what you find in .env.sample **You should paste this whole thing into the `GOOGLE_SERVICE_ACCOUNT` environment variable on the Vercel dashboard for your own deployment of opensheet.**

## Local development

Install the [Vercel CLI](https://vercel.com/cli), and then run:

```sh
vercel dev
```
