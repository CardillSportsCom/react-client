# React & Firebase Starter

## Tech Stack

* [Firebase](https://firebase.google.com/) - Firestore database, auth, cloud functions, local emulators
* [React](https://reactjs.org/)
* [Webpack](https://webpack.js.org/)
* [Tailwind CSS](https://tailwindcss.com/)
* [React Router](https://reactrouter.com/web)
* [react-firebase-hooks](https://github.com/CSFrequency/react-firebase-hooks/)
* [React Helmet](https://www.npmjs.com/package/react-helmet) - SEO
* [Mocha](https://mochajs.org/) - testing for Firebase
* [ESLint](https://eslint.org/) - based on AirBnB config

### Prerequisites

You will need the following to use this starter: 

* [Node](https://nodejs.org/en/)
* [Java DK](https://docs.oracle.com/en/java/javase/16/install/overview-jdk-installation.html#GUID-8677A77F-231A-40F7-98B9-1FD0B48C346A)
* A Firebase project created in [Firebase Console](https://console.firebase.google.com)

## Setup Guide

Clone this repo:
```git clone https://github.com/dariatsvetkova/firebase-boilerplate-draft.git```


Install the dependencies:
```cd .\firebase-boilerplate-draft\ && npm install```

Do the same in the `/functions` folder to use Firebase cloud functions:
```cd functions && npm install```

At this point, the client side should work. You can launch it with:
```cd .. && npm start``` 

### Firebase Setup

You may have noticed that data isn't yet being fetched from Firebase. We need to connect a Firebase project to make it work.

In [Firebase Console](https://console.firebase.google.com), enable Firestore Database and Authentication via Google.

Back to your code editor, open a new terminal. Log into Firebase CLI:
```cd .\firebase-boilerplate-draft\ && firebase login```

Start connecting your Firebase project:
```firebase init```
and follow the prompts. **When asked if you'd like to overwrite existing files, choose 'No'.**

This project is set up to use Firestore, Functions, and Emulators. Make sure you choose these options when prompted by Firebase CLI. Similarly, when asked about which emulators you want to use, choose Auth, Firestore, and Functions.

Now that we've initialized the local Firebase directory, let's connect it to your project.

Run `firebase projects:list` and copy the ID of the project you want to use.

Then tell Firebase CLI to use that project:
```firebase use <your project ID>```

Head over to `/src/firebase.clientApp.js` and add your config object (found in Firebase Console under Project Settings).


`firebase init firestore` to initialize rules and functions
Set up rules, functions


`firebase deploy` to update rules and functions  —  will complain about functions on a free plan
After that, use emulators for local development instead



## Usage

### Build

```npm start```

### Test

```npm run emulators```
In another terminal: `npm test`

You should see a list of 3 tests that all pass. 
### Deploy

```npm run build```

## Purpose
Some stuff

## Contribute
Other stuff

## Licence
Some stuff
