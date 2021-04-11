![image](https://user-images.githubusercontent.com/36793262/112931849-9eb1a280-9168-11eb-9927-19e83f790cef.png)

This repo contains the follwing YAML based Azure Pipeline defintions

- sfpowerscripts-prepare.yml
   Pipeline demonstrating how prepare command is used to build scratch org pools
   
- sfpowerscripts-validate.yml
   Pull Request Validation Pipeline, that validates incoming changes against a scratch org fetched from the pool
   
- sfpowercripts-build-deploy.yml
   Pipeline that gets triggered on a merge to the trunk, resulting in building a set of packages, deploying to scratch org to validate (in real life scenarios, you would replace this with a sandbox) and then build a set of validated packages and finally publis that to artifact repository

- sfpowerscripts-fetch-release.yml
   A release pipeline that utilizes the release defintion to fetch artifacts from artifactory and then deploy to a sandbox (simulated using scratch org for example purposes)



The sample pipelines utilise an azure pipelines variable group called DEVHUB which contains the following variables. As a prerequisite, this has to be setup manually
- DEVHUB_USERNAME   : The username of the DevHub org
- DEVHUB_CLIENT_ID  : The client id of the connected app that is used to authenticate a JWT based authentication to the DevHub

A secure file should also be placed in the library which is the public key file used for JWT authentication
- DEVHUB_SERVER_KEY : A file that contains the key used for JWT server authentication

For more information, follow the links here https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/sfdx_dev_auth_jwt_flow.htm

