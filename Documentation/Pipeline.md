## Pipeline process

CircleCi detects the changes in the repo's master branch and starts the pipeline.
The pipeline is as follows:
* Install NodeJs
* Install NPM
* Checkout the code
* Install AWS CLI
* Install Elastic Beanstalk CLI
* Installs dependency for Front-End Application using `npm run frontend:install`
* Installs dependency for Back-End Application using `npm run backend:install`
* Builds Front-End Application using `npm run frontend:build`
* Builds Back-End Application using `npm run backend:build`
* Deploy Front-End Application using `npm run frontend:deploy`
* Deploy Back-End Application using `npm run backend:deploy`

**Pipeline is configured in `.circleci/config.yml`**