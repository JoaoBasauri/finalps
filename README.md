# Preganancy safe



Standard Web App for Tech Communties. <br>
[Demo](https://myaurapp.web.app/) <br>
Version: 3.1.1

### Show some :heart: and star the repo to support the project
### If you are using Aura, Kindly [fill this form](https://forms.gle/SNpajdAnqbSac2AV9) for Aura Web App Directory

## Overview

Aura is the Web App that helps you to mange the Tech Communities like GDGs, DSCs or any other tech communities with Aura Admin.

## Features
| Feature | Description |
|---|---|
| **Fast and optimized** | PWA on Lighthouse |
| **Works offline** | Can work offline |
| **Dark/Light Theme Mode** | Light/Dark Theme Mode |
| **Mobile first** | Mobo Friendly Web app can be installed as a native app on your phone |
| **SEO optimized** | index all content and get to the top in search results |
| **Easy in management** | Easy in Management by using Aura Admin |
| **Trigger Push Notification** | Trigger Push Notification to Aura Main |
| **Usability** | Any Tech Communities can use |
| **Custom Event Page** | Now No need to create the website for XYZ event |
| **Public shareable URL for Team & Speakers** | Team member public URL for Self Branding and Public Speaker Directory & Public URL for Promotion |


1. In the Firebase project console dashboard. Click on create new web app
1. Go to Firebase project Settings and then General Settings Tab
1. Scroll down and go to your app section under Firebase SDK snippet
1. Now click on the config
1. Copy the code which looks similar to the below sample
    ```js
    apiKey: "Axxxxxxxxxxxxxxxxxxx",
    authDomain: "xxxxxx.firebaseapp.com",
    databaseURL: "https://xxxxxxxx.firebaseio.com",
    projectId: "xxxxxxxxx",
    storageBucket: "xxxxxxx.appspot.com",
    messagingSenderId: "xxxxxxxxxxx",
    appId: "1:xxxxxxxxx:web:xxxxxxx"
    ```
1. Now goto project code and inside [src/config/](https://github.com/gdg-x/aura/blob/master/src/config/firebase.js) update the `firebase.js` file with these codes
1. Update the field name in [vue.config](https://github.com/gdg-x/aura/blob/master/vue.config.js)
1. Run locally
    - `npm run serve`
    - For the First Time you will see a text Either `Your Internet is not Working or Site is not Configured`
1. For the production: `npm run build` and then one dir will be created dist
1. For testing: `npm run test`
1. Setup [Aura Admin](https://github.com/gdg-x/aura-admin/fork) for Management of Aura v3

## Deployment on Firebase
1. Install required tools for performing Firebase deployment
    - Install Firebase CLI: `npm i -g firebase-tools`
1. Login into Firebase CLI using the following command -  `firebase login`
1. Open Terminal/CMD/Powershell in the root directory of your clone of aura-admin repository.
1. Now type `firebase login` command in your Terminal/CMD/Powershell
1. Update the `Firebase Project ID` in `.firebasesrc` file. This value should match the project ID in your Project Settings of the Firebase project you created in the previous section.
1. Go to the Firebase Console Dashboard and Click on Hosting in the left navigation.
1. Click on Get Started
1. Click through all steps till you’re taken to the Hosting page in the console.
1. You’ll be provided with a ready domain with your project ID. It should look like - `<project-id>.web.app or <project-id>.firebaseapp.com`
1. Copy the sub-domain name of the URL provided. In this case, it will be the project ID. However, to be precise, you have to copy the part before .web.aap or .firebaseapp.com. This is your Site ID
1. Update `Firebase.json` file, set the site key to Site ID
    ```js
        {
            "hosting": {
                "site":"Your_Firebase_Hosting_id",
                "public": "dist",
                "rewrites": [ {
                    "source": "**",
                    "destination": "/index.html"
                } ],
                "ignore": [
                    "firebase.json",
                    "**/.*",
                    "**/node_modules/**"
                ]
            }
        }
    ```
1. In your terminal at the root directory of the project,  build and deploy using the following command     
    - `firebase deploy`




### Documentation
1. [Full documentation](https://docs.google.com/document/d/18jKhG10OZx1T87ey8rtLYjyPpjPTCqPfX3JiOs3PUcs/edit?usp=sharing).


## Technology Stack

* [VueJS](https://vuejs.org/)
* [Vuetify](https://vuetifyjs.com/en/)
* [Firebase](https://firebase.google.com/)
* [Service Worker & PWA](https://www.npmjs.com/package/vue-pwa)
* [Workbox](https://developers.google.com/web/tools/workbox)



## Contributing

Awesome! Contributions of all kinds are greatly appreciated. To help smoothen the process we have a few non-exhaustive guidelines to follow which should get you going in no time.

### Using GitHub Issues

- Feel free to use GitHub issues for questions, bug reports, and feature requests
- Use the search feature to check for an existing issue
- Include as much information as possible and provide any relevant resources (Eg. screenshots)
- For bug reports ensure you have a reproducible test case
 - A pull request with a breaking test would be super preferable here but isn't required

### Submitting a Pull Request

- Squash commits
- Lint your code with eslint (config provided)
- Include relevant test updates/additions
- Pull requests _must_ be made against `develop` branch. Any other branch (unless specified by the maintainers) will get rejected.

## Contributors
<b>Maintainer:</b> [Vrijraj Singh](https://github.com/vrijraj) <br>
<b>Developers:</b> [Vrijraj Singh](https://github.com/vrijraj) &  [Bharat Agarwal](https://github.com/bharatagsrwal) 

### View Website Built with Projects

| Community Name | Web App Link |
| --- | --- |
| GDG Jalandhar | [View Now](https://gdgjalandhar.com) |
| DSC NSEC | [View Now](https://dscnsec.com) |
| GDG Konya | [View Now](https://gdgkonya.com) |


## Facing Any Problem or need any Help?
Write us in [issues](https://github.com/gdg-x/aura/issues) section. Our team will try solve your issue within 10-12 hours.<br>
