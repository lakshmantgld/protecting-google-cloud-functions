# protecting-google-cloud-functions
This repo contains the examples, reference documents mentioned in this [medium post]().

### Technical Architecture
![Technical Architecture](https://raw.githubusercontent.com/lakshmantgld/protecting-google-cloud-functions/master/doc/protecting-google-cloud-functions.png)

### Installation & Setup
1. Install functions emulator `npm install -g @google-cloud/functions-emulator` to test your functions locally.
2. Create and download the Firebase `service account` and name it as `serviceAccount.json`. Check out `serviceAccount.copy.json` for your reference.
3. Create and download the Google Cloud Platform service account to deploy cloud functions. Follow the [tutorial](https://serverless.com/framework/docs/providers/google/guide/credentials/) to setup the serverless framework with Google Cloud.
4. Duplicate the `config.copy.yml` file and rename it as `config.yml`. Add the Google Cloud `projectId` and `credentials`(service account) file path to the `config.yml`.

### Local Development
`functions emulator` helps to test your google cloud functions locally.
1. Start the emulator by running `npm run emulator`.
2. Deploy your functions locallt by running `npm run local`.
3. Now, you can test it with URL that you received from **step 2**.
4. Make sure, you attach the firebase ID token to the `Authorization` header of each request.

### Deployment
1. Deploy your functions to google cloud by running `npm run deploy`.
2. Now, you can test it with URL that you received from **step 1**.
3. Make sure, you attach the firebase ID token to the `Authorization` header of each request.