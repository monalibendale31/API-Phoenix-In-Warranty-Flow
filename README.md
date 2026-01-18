# Postman API Automatomation Integration with Github Actions

This responsitory is a demonstartion for POC for integrating postman tests with github actions. The tests are written in postman and thet are executed on the VM with the help of newman and newman-reporter-htmlextra
Github actions will trigger the project execution on every push to the main branch.Youcan also execute the project manually using workflow_dispatch. The projects runs on a scheduled time with the help of the cron job.

The HTML report is archieved and kept in the artifact section for the team to download it. Along with that they can view the reprt directly from https://monalibendale31.github.io/API-Phoenix-In-Warranty-Flow/
The lastet report is mailed to team members using GMAIL SMTP.

## Tech stack##
1. Postman
2. Node js 24v
3. Newman
4. Newman-reporter-htmlextra
5. Github actions
6. Gmail SMTP
7. Github pages
8. CSV for Data Driven Testing.
9. AWS-EC2 instance for self hosted github runner.

## Github Pages ##
You can directly view the latest report of the postman Test at the github page link : https://monalibendale31.github.io/API-Phoenix-In-Warranty-Flow/

## How to run the project? ##
You can run the project on your local system for that:
1. Clone the project on your local system : https://github.com/monalibendale31/API-Phoenix-In-Warranty-Flow.git
2. Install Node js and npm from https://nodejs.org/en
3. Install Newman using $ npm install -g newman
4. Install newman-html-reporter using this command $ npm install -g newman-reporter-html
5. run the newman command:
   newman run "Inwarranty-flow Collection.postman_collection.json" \
            -e QA.postman_environment.json \
            -d testData.csv \
            -r cli,htmlextra \
            --reporter-htmlextra-export ./newman/index.html
## HTML Report ##
the report will be created in the newman folder
![Postman Report](https://github.com/monalibendale31/API-Phoenix-In-Warranty-Flow/blob/static-content/newman%20report.jpg)
