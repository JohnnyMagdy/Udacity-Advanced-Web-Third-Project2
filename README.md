# Hosting a Full-Stack Application

In this project I learned how to take a newly developed Full-Stack application built for a retailer and deploy it to a cloud service provider so that it is available to customers. I used the aws console to start and configure the services the application needs such as a database to store product information and a web server allowing the site to be discovered by potential customers. I modifyd package.json scripts and replaced hard coded secrets with environment variables in my code.

After the initial setup, I learnd to interact with the services started on aws and deployed manually the application on my first time to it. As I got more familiar with the services I interacted with them through a CLI.

Then I registered for a free account on CircleCi and connected my Github account to it. Based on the manual steps used to deploy the app, I wrote a config.yml file that will make the process reproducible in CircleCi. I set up the process to be executed automatically based when code is pushed on the main Github branch.

The project will also include writing documentation and runbooks covering the operations of the deployment process. Those runbooks will serve as a way to communicate with future developers and anybody involved in diagnosing outages of the Full-Stack application.

# Udagram

The udagram application is a fairly simple application that includes all the major components of a Full-Stack web application.



### Dependencies

```
- Node v14.15.1 (LTS) or more recent. While older versions can work it is advisable to keep node to latest LTS version

- npm 6.14.8 (LTS) or more recent, Yarn can work but was not tested for this project

- AWS CLI v2, v1 can work but was not tested for this project

- A RDS database running Postgres.

- A S3 bucket for hosting uploaded pictures.

```

### Installation

Provision the necessary AWS services needed for running the application:

1. In AWS, provision a publicly available RDS database running Postgres.
1. In AWS, provision a s3 bucket for hosting the uploaded files.
1. Export the ENV variables needed or use a package like [dotnev](https://www.npmjs.com/package/dotenv)/.
1. From the root of the repo, navigate udagram-api folder `cd starter/udagram-api` to install the node_modules `npm install`. After installation is done start the api in dev mode with `npm run dev`.
1. Without closing the terminal in step 1, navigate to the udagram-frontend `cd starter/udagram-frontend` to intall the node_modules `npm install`. After installation is done start the api in dev mode with `npm run start`.

## Testing

This project contains two different test suite: unit tests and End-To-End tests(e2e). Follow these steps to run the tests.

1. `cd starter/udagram-frontend`
1. `npm run test`
1. `npm run e2e`

There are no Unit test on the back-end

### Unit Tests:

Unit tests are using the Jasmine Framework.

### End to End Tests:

The e2e tests are using Protractor and Jasmine.

## Built With

- [Angular](https://angular.io/) - Single Page Application Framework
- [Node](https://nodejs.org) - Javascript Runtime
- [Express](https://expressjs.com/) - Javascript API Framework
  
##  link to a hosted working Front-End Application
  [Link](http://randomudacity1233215.s3-website-us-east-1.amazonaws.com/)
  
## CircleCi
  Images added as CircleCi 1.png, CircleCi 2.png, and CircleCi 3.png in the root dir

## Configuration page of my AWS services
  In root directory images added as:
  1. RDS:
     - RDS config 1.png
     - RDS config 2.png
  2. EB: EBConfig.png
  3. S3:
     - S3 bucket config 1.png
     - S3 bucket config 2.png
