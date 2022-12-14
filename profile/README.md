# 🙋‍♀️ this is my-club app | the next generation 👋
myclub App is the way for floorball, handball & volleyball clubs in switzerland to manage their club. Based on real data from swissunihockey, swiss volley and swiss handball association, we generate real value for the users, so they can focus an what matters most, their success!

# 🌈 Contribution guidelines - how can you be a part of it?
todo :)

# 👩‍💻 Useful resources - where did you get the relevant information?
myclub App's architecture follows these principles:
- mobile first
- always bet on the web
the latest version of the app is always available as PWA. In a second stage we also support iOS and Android Apps.

## Backend Data
We use a GraphQL API for Sports Data. Check this [repository](https://github.com/myclubapp/backend).

# 👨‍💻 Developer
## Create App Icon & Splash Screen
- Generate your app icon and splash screens using cordova-res --skip-config --copy
- Icon generator for manifest [Link](https://manifest-gen.netlify.app/)
- Favicon generator [Link](https://www.hoststar.ch/de/tools/favicon-generator)
- Install Asset generator: ``npm install --global pwa-asset-generator`` and run commands: 
Light Mode: ``pwa-asset-generator ./resources/icon.png -i ./src/index.html -m ./src/manifest.webmanifest --splash-only --dark-mode -p 0% ``
- Dark Mode: ``pwa-asset-generator ./resources/icon_dark.png -i ./src/index.html -m ./src/manifest.webmanifest --splash-only -p 0%  ``

## Native
- Run ionic capacitor add to add a native iOS or Android project using Capacitor

## Web
- Run ionic serve within the app dpy

## Installed packages
- Tailwind CSS (``npm install -D tailwindcss@latest postcss autoprefixer``)
- Capacitor JS (V3)
- Ionicframework (V6)
- Angular PWA (``ng add @angular/pwa --project _project-name_``)
- Apollo Angular (``ng add apollo-angular``)
- [Angular Localize](https://angular.io/guide/i18n-common-locale-id) 
-- de-CH 	German (Switzerland)
-- fr-CH 	French (Switzerland)
-- it-CH    Italian (Switzerland)
-- en-US    English
- Angular Fire ``ng add @angular/fire``
- Fontawesome Icons
- Ionicons


# 🚨 CUSTOM Apps

## Available Custom Apps: 
- Kadetten Unihockey Schaffhausen [Link](https://kadetten-unihockey.web.app)
- UHC Winterthur United [Link](https://uhc-win-u.web.app)

## General new custom app
Go to CUSTOM_THEMES and copy default folder. Then create icons and the following files change: 
- index.html
- tailwind.config.js [This is still an issue]
- webmanifest.manifest

### Add Default Sites
firebase target:apply hosting app-unihockey unihockey

### Add Custom Sites
firebase target:apply hosting app-FIREBASE_SITE_MYAPP FIREBASE_SITE_MYAPP

### Remove
firebase target:remove hosting FIREBASE_SITE_MYAPP

### Icon
Run commands to generate custom icons: 
pwa-asset-generator ./resources/app-CUSTOM_icon.png --splash-only --dark-mode -p 0%
pwa-asset-generator ./resources/app-CUSTOM_icon.png  --splash-only -p 0%
pwa-asset-generator ./resources/app-CUSTOM_icon.png  --icon-only --dark-mode -p 0%

then, copy icons to src/custom_themes/app-CUSTOM/assets
- /icons
- /splash

Also upload login.jpg to /bg and create favicon.


# 🍿 Just for fun
App build: [![Build + Prerender + Deploy](https://github.com/myclubapp/app/actions/workflows/main.yml/badge.svg)](https://github.com/myclubapp/app/actions/workflows/main.yml)

Backend build: [![Build + Deploy](https://github.com/myclubapp/backend/actions/workflows/main.yml/badge.svg)](https://github.com/myclubapp/backend/actions/workflows/main.yml)
