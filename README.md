<h1 align="center">Unused CSS Remover</h1>

<div align="center">
  :steam_locomotive::train::train::train::train::train:
</div>
<div align="center">
  <strong>A NodeJS project</strong>
</div>
<div align="center">
  A simple tool that uses Google Chrome to detect and remove unused CSS from website
</div>

<br />

<div align="center">
  <!-- Stability -->
  <a href="https://nodejs.org/api/documentation.html#documentation_stability_index">
    <img src="https://img.shields.io/badge/stability-experimental-orange.svg?style=flat-square"
      alt="API stability" />
  </a>
  <!-- NPM version -->
  <a href="https://npmjs.org/package/choo">
    <img src="https://img.shields.io/npm/v/choo.svg?style=flat-square"
      alt="NPM version" />
  </a>
  <!-- Standard -->
  <a href="https://standardjs.com">
    <img src="https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat-square"
      alt="Standard" />
  </a>
</div>

<div align="center">
  <sub>The little script is designed ❤︎ by
  <a href="https://twitter.com/amit08255">Amit Kumar</a>
</div>

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Getting Started](#getting-started)
- [Example](#example)
- [How It Works](#how-it-works)
- [License](#licens)
- [Contact](#contact)

## Introduction
This is simple script designed in NodeJS and uses Google Chrome code coverage tool for the purpose of removing unused CSS.
The working mechanism of this tool is different from others. The unused CSS remover tools available today, scans and removes CSS but they also removes those CSS styles which are dynamically used by JavaScript. This tool uses Google Chrome browser and its CSS code coverage tool to remove unused CSS.

## Features
- __small:__ this script is very simple and small
- __pseudoclass supported:__ supports CSS pseudoclasses like - hover
- __dynamic css supported:__ can extract CSS classes added dynamically by JavaScript


## Installation
1. Install NodeJS on your system.

2. Clone this repository.

3. Run below command in terminal to install all dependencies -
```sh
npm install
```

## Getting Started

Install **Google Chrome** browser, if you haven't already.
Now you need to launch **Google Chrome** with remote debugging enabled. Run below command in order to do that -

* For Windows
```sh
start chrome.exe –remote-debugging-port=8000
```

* For MAC OS
```sh
/Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome --remote-debugging-port=9222 --no-first-run --no-default-browser-check --user-data-dir=$(mktemp -d -t 'chrome-remote_data_dir')
```

* For Linux
```sh
google-chrome   --remote-debugging-port=8000
```

Now the Google chrome will be started with remote debugging server at port - 8000

When server is started you are provided an URL like --  ws://127.0.0.1:8000/devtools/browser/82ee571e-8485-4514-ae74-34b6affbad3b
Copy the URL we will need that later.


Now run our NodeJS script using below command -

node   cleaner.js   url_copied_above   link1  link2  link3

In above command link1, link2 and link3 are links of same website that you want to open for extracting unused CSS.


## Example
```sh
node cleaner.js ws://127.0.0.1:8000/devtools/browser/82ee571e-8485-4514-ae74-34b6affbad3b http://localhost:7000 http://localhost:7000/centre/2 http://localhost:7000/login
```
Above command will launch our script and open urls - http://7000, http://7000/centre/2 and http://localhost:7000/login one by one to scan the CSS.

## How It Works
Once the script is started, it will open link in Chrome browser, you now have to use the website (move mouse over button, resize screen, and use other functions) this will be used to extract all the CSS that are left behind (or not scanned). Just remember, your action should not redirect to other page or the script will not work properly for opened URL. Also remember that the URL that, if your website has section that requires login, you need to login before using website in script and for pages that needs to logout, clear cookie before opening that page in script. Every time a page is opened, the scripts pauses and asks to press any key to continue, this feature is added so that you can interact with your website page before continuing to next one so that CSS is extracted well.
Once the CSS file is saved, press Ctrl+C to exit the script.
A CSS file named - final_css.css is created with extracted CSS from website.

## License
[MIT](https://tldrlegal.com/license/mit-license)

<!-- CONTACT -->
## Contact

Amit Kumar - [@amit08255](https://twitter.com/amit08255) - amitcute3@gmail.com

Project Link: [https://github.com/amit08255/unused-css-remover](https://github.com/amit08255/unused-css-remover)

