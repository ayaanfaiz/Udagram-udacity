## Front-End Infrastructure:

The frontend application uses Angular 8 for the application development.
It is build and then hosted on AWS S3 Service. Here is the link to the application: [Udagram](http://udagram-fe.s3-website-us-east-1.amazonaws.com/)

## BackEnd-Application

The backend application is developed using Express with TypeScript. 
It is build and then uploaded to a Elastic Beanstalk application with follows theses steps:
* Uploads the source code to the S3 service.
* Starts updating the environment. In our case it's `udagram-udacity-env`
* Deploys the newly uploaded application to EC2. The application name is `udagram-udacity`
* Once this is done, the environment update completes successfully.

## Deployment Pipeline

The app is automated with a CircleCi pipeline service with the Github repository - `Udagram-udacity`.
As soon as we push to the master branch of the Git repo, the CircleCi detects the changes and starts the pipeline to deploy the new changes.