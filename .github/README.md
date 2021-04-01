Easy Spaces Lightning Web Components Sample Application using sfpowerscripts Orchestrator
This repo demonstrates how sfpowerscripts orchestrator can be used across lifecycle of your project. Sample pipelines are available for GitHub Actions and Azure Pipelines.

Read more about sfpowerscripts at https://dxatscale.gitbook.io/sfpowerscripts/

Steps:

- Ensure the pre-requisites are place in your DevHub

- Enable DevHub
- Enable 2GP Packaging
- Install the necessary pre-requisites for scratch org pooling, especially Step 1. Read more from https://github.com/Accenture/sfpowerkit/wiki/Getting-started-with-ScratchOrg-Pooling

- Install sfpowerkit locally

- Install sfpowerscripts in your local system

- Run sfdx sfpowerscripts:orchestrator:build -v devhub from the project directory (Please make sure you create these unlocked packages and its versions first in your devhub before proceeding using regular sfdx commands!)

- Now use the sample pipelines to understand prepare, validate and deploy

Fork it! and test it yourself
