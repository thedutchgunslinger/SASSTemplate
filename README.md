
- [NL](#nl)
  - [Installatie](#installatie)
    - [Stap: 1](#stap-1)
    - [Stap 2:](#stap-2)
    - [Stap 3:](#stap-3)
  - [Handmatige installatie](#handmatige-installatie)
    - [Stap: 1](#stap-1-1)
    - [Stap: 2](#stap-2-1)
    - [Stap: 3](#stap-3-1)
    - [Stap: 4](#stap-4)
- [ENG](#eng)
  - [Installation](#installation)
    - [Step: 1](#step-1)
    - [Step 2:](#step-2)
    - [Step 3:](#step-3)
  - [Manual installation](#manual-installation)
    - [Step: 1](#step-1-1)
    - [Step: 2](#step-2-1)
    - [Step: 3](#step-3-1)
    - [Step: 4](#step-4)
# NL
## Installatie
### Stap: 1
Clone de repository voor eigen gebruik.
### Stap 2:
Open de terminal en run ```npm install```
### Stap 3: 
Run in de terminal ```npm run start```

Happy coding! 🎊
## Handmatige installatie
### Stap: 1
Maak deze folder structuur aan in je project:
```
└───src
|   ├───assets
|   └───js
|   |   └───main.js
|   └───sass
|   |   └───styles.scss
|   └───index.html
└───package.json
```
### Stap: 2
Kopieer deze code in je ```package.json``` bestand.
```json
{
  "name": "project",
  "version": "0.1.0",
  "description": "SASS compile|autoprefix|minimize and live-reload dev server using Browsersync for static HTML",
  "main": "public/index.html",
  "author": "Noah Beij",
  "scripts": {
    "build:sass": "sass  --no-source-map src/sass:public/css",
    "copy:html": "copyfiles -u 1 ./src/*.html public",
    "copy:assets": "copyfiles -u 1 ./src/assets/**/* public",
    "copy:js": "copyfiles -u 1 ./src/js/**/* public",
    "copy": "npm-run-all --parallel copy:*",
    "watch:html": "onchange \"src/*.html\" -- npm run copy",
    "watch:assets": "onchange \"/src/assets/**/*\" -- npm run copy:assets",
    "watch:js": "onchange \"/src/js/**/*\" -- npm run copy",
    "watch:sass": "sass  --no-source-map --watch src/sass:public/css",
    "watch": "npm-run-all --parallel watch:*",
    "serve": "browser-sync start --server public --files public",
    "start": "npm-run-all copy --parallel watch serve",
    "build": "npm-run-all copy:html build:*",
    "postbuild": "postcss public/css/*.css -u autoprefixer cssnano -r --no-map"
  },
  "dependencies": {
    "autoprefixer": "^10.4.2",
    "browser-sync": "^2.27.7",
    "copyfiles": "^2.4.1",
    "cssnano": "^5.0.17",
    "npm-run-all": "^4.1.5",
    "onchange": "^7.1.0",
    "postcss-cli": "^9.1.0",
    "sass": "^1.49.8"
  }
}
```
### Stap: 3
Open de terminal en run ```npm install```
### Stap: 4
Run in de terminal ```npm run start```

Happy coding! 🎊
# ENG
## Installation
### Step: 1
Clone the repository for your own use.
### Step 2:
Open the terminal and run ```npm install```
### Step 3: 
Run in the terminal ```npm run start```

Happy coding! 🎊
## Manual installation
### Step: 1
Make this folder structure in your own project:
```
└───src
|   ├───assets
|   └───js
|   |   └───main.js
|   └───sass
|   |   └───styles.scss
|   └───index.html
└───package.json
```
### Step: 2
Copy this code in your own ```package.json``` file.
```json
{
  "name": "project",
  "version": "0.1.0",
  "description": "SASS compile|autoprefix|minimize and live-reload dev server using Browsersync for static HTML",
  "main": "public/index.html",
  "author": "Noah Beij",
  "scripts": {
    "build:sass": "sass  --no-source-map src/sass:public/css",
    "copy:html": "copyfiles -u 1 ./src/*.html public",
    "copy:assets": "copyfiles -u 1 ./src/assets/**/* public",
    "copy:js": "copyfiles -u 1 ./src/js/**/* public",
    "copy": "npm-run-all --parallel copy:*",
    "watch:html": "onchange \"src/*.html\" -- npm run copy",
    "watch:assets": "onchange \"/src/assets/**/*\" -- npm run copy:assets",
    "watch:js": "onchange \"/src/js/**/*\" -- npm run copy",
    "watch:sass": "sass  --no-source-map --watch src/sass:public/css",
    "watch": "npm-run-all --parallel watch:*",
    "serve": "browser-sync start --server public --files public",
    "start": "npm-run-all copy --parallel watch serve",
    "build": "npm-run-all copy:html build:*",
    "postbuild": "postcss public/css/*.css -u autoprefixer cssnano -r --no-map"
  },
  "dependencies": {
    "autoprefixer": "^10.4.2",
    "browser-sync": "^2.27.7",
    "copyfiles": "^2.4.1",
    "cssnano": "^5.0.17",
    "npm-run-all": "^4.1.5",
    "onchange": "^7.1.0",
    "postcss-cli": "^9.1.0",
    "sass": "^1.49.8"
  }
}
```
### Step: 3
Open the terminal and run ```npm install```
### Step: 4
Run in the terminal ```npm run start```

Happy coding! 🎊
