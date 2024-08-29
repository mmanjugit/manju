# Management Portal

## Summary
This repository contains the front-end code for the new TF Connect management portal. It is written in Vue 3 (with Composition API) with Bootstrap 5. This portal can be used to onboard new Companies, Merchants and Attendants with different Roles and Groups, it supports to configure Gateways and also can perform different POS Transactions.

### List of functionalities offered by the portal
* The login and logout pages for users of any role in the portal will be used for user authentication.
* Verify OTP, resend OTP, forgot password, change password, reset password functionalities will be provided as a security feature to our portal.
* Create, view, edit, search, delete functionalities will be provided for a Company, Merchant and Attendant.
* Create, search, disable functionalities will be provided for a user.
* Associations to an user can be made with company/merchant/attendant in the portal.
* Lifecycle of a user consists of the following status: `Pending`, `Not Associated`, `Active`, `Deleted`, `Locked`.
* Groups permission can be configured once which can be reused while assigning permissions to users.
* Users can be assigned permissions dynamically based on feature selections.
* Users will be able to view transaction list with advance search and filtering techniques with detailed view of a specific transaction.
* The user guides are available to download based on the logged in user role which helps the user to interact with the portal with ease.
* Users will have the ability to view and download user audit report to track user login and logout activities to the portal.
* As a security feature, automatic logout functionality will be provided to the user to handle user inactivity with the portal

## Developer Setup
The following software configuration is used during development:

* Node.js - v. 14.17.0
* npm - v. 6.14.13
* @vue/cli - v. 4.5.13
* Git
* GitFlow workflow
* Visual Studio Code
* Visual Studio Code Extensions:- 
  * Autorename Tag
  * Vetur
  * es-string-html
  * Bracket pair colorizer
  * vscode-icons
  * Prettier

## Branches and Branching Strategy
The main Git branch is called `master` which is used for production. A long lived branch called `development` also exists that runs parallelly with `master` branch which will be used by all the developers to keep track of the latest code.

The project exclusively uses Git-Flow branching strategy invented by Vincent Driessen.
<p align="center">
  <br>
  <img src="https://www.linkpicture.com/q/git-strategy.png" height="400" width="600" />
  <br>
</p>

## Installation

If you would like to run the TF Connect management portal on your local machine, you will need to follow these instructions:

```sh
$ git clone git@bitbucket.org:tf-connect/management-portal.git
$ cd management-portal
$ npm install
```

You should have [nginx-1.22.0](http://nginx.org/download/) in any preferred path in your system. Run nginx using the command 'start nginx'. Replace the content in the `nginx.conf` file with the mentioned code in [this file](https://bitbucket.org/tf-connect/management-portal/src/development/nginx-conf.md).

### Before running the frontend portal, follow the instructions provided in the below backend repositories:

- Portal service

- Identity service

- Email service
 

## Running the frontend portal application
Note: After the above services are successfully running in your local development environment, get started with running the frontend portal service now.

Create `.env.development` file in the root of the project and put in the following code to it and save.

```sh
VUE_APP_API_GATEWAY_URL=<VALUE_HERE>
```
All the `npm` commands that can be run for the project are defined in the `"scripts"` section of *package.json*.

#### Run development server (with hot-reload)

```sh
npm run serve
```

#### Compile and minify for production

```sh
npm run build
```

#### Run unit tests

```sh
npm run test:unit
```

#### Lint with ESLint

```sh
npm run lint
```

## License and copyright info
(c) 2022 - Present, ThoughtFocus. All right reserved"# manju" 
