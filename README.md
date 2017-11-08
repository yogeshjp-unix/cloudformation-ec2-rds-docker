# cloudformation-ec2-rds-docker
AWS Cloudformation to deploy Rail API application on Docker containers - hosted on EC2 Host and AWS RDS Instance for MySQL.

# Setup AWS & CLI

* Login to AWS Management Console 
* Generate a KeyPair. Save the downloaded key to access the environment.
* Configure AWS Command Line Interface (AWS CLI) with a new AWS Access Key and a secret generated on AWS.
* Update the stack.yml using this template for your application
* Use AWS CLI to run aws cloudformation create-stack command that'll create all the resources defined in the stack.yml
  ** Creates the Application node EC2 - We will turn this host into a docker host
  ** Deploys Application Security Group
  ** Creates the RDS Database - MySQL engine
  ** Deploys RDS Security Group
* Update the docker-compose app.yml using this template for your application
  ** Deploys the Application container - Rails API on the EC2 docker host
  ** Prepared the environment and connectivity to the Database
  ** Creates a WebServer (PHP/Apache) to render contents  
* Using docker compose run database migration command, run service in background and run db-seed to populate test data
  ** Access the API over the IP returned by the App Node and retrieve the contents of the API's
  ** Use InSomnia


# Have fun
