This is a demo which I did for .Net Conf 2021 in Taiwan for the session about Azure Communication Service.

The original of the content is from Microsoft tutorial content, which links are give in each section.

## Getting user access token and user id
You can get user access token and user id (who you want to call) by using Azure Portal `Identities & User Access Tokens` function

![Identities & User Access Tokens](img\azure-portal-identity.png)

## demo-01-1on1

### setup
The purpose of this demo is to show how easily creating a 1 on 1 voice call can be set up

What you will need to do is:
1. run `npm i`
2. call `npx webpack-dev-server --entry ./client.js --output bundle.js --debug --devtool inline-source-map`
3. navigate to [http://localhost:8080/](http://localhost:8080/) on your browser

### running
The js has been setup to call the echo phone - use for testing purpose.
If you want to call the reall user, change line 34 of [client.js](demo-01-1on1\client) to
```
        [{ communicationUserId: userToCall }],
```

### detail description
[Quickstart: Add voice calling to your app](https://docs.microsoft.com/en-us/azure/communication-services/quickstarts/voice-video-calling/getting-started-with-calling?pivots=platform-web&WT.mc_id=AZ-MVP-5003856)

## demo-02-1on1-video-call

### setup
The purpose of this demo is to show how easily creating a 1 on 1 video call can be set up

What you will need to do is:
1. run `npm i`
2. call `npx webpack-dev-server --entry ./client.js --output bundle.js --debug --devtool inline-source-map`
3. navigate to [http://localhost:8080/](http://localhost:8080/) on your browser

### running
You can open two browser instance, represent the participant of the call.
Generate two user Id and token, the token use to initalize call and the callee will be the user Id
If your computer/laptop support two camera (such as Surface Book 3), you can1change1 the drop down from 0 and 1 respectively

### detail description
[QuickStart: Add 1:1 video calling to your app](https://docs.microsoft.com/en-us/azure/communication-services/quickstarts/voice-video-calling/get-started-with-video-calling?pivots=platform-web&WT.mc_id=AZ-MVP-5003856)


## demo-03-join-teams

### setup
The purpose of this demo is to show how easily join a teams meeting using anonymous

What you will need to do is:
1. run `npm i`
2. change [client.js](demo-03-join-teams\client.js) line 15 of `<access token>` to the accual access token of your user
3. call `npx webpack-dev-server --entry ./client.js --output bundle.js --debug --devtool inline-source-map`
4. navigate to [http://localhost:8080/](http://localhost:8080/) on your browser

### running
1. You should create a teams meeting and get the invite link and input in the `Teams meeting link input box`
2. click `Join Teams Meeting` and you should see a user waiting in the lobby in Teams meeting

### detail description
[Quickstart: Join your calling app to a Teams meeting](https://docs.microsoft.com/en-us/azure/communication-services/quickstarts/voice-video-calling/get-started-teams-interop?pivots=platform-web&WT.mc_id=AZ-MVP-5003856)
