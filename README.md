# Postman API Automation Integration with GitHub Actions #

This repository is the demonstration for POC for integrating our postman tests with GitHub Actions. The tests are written in postman and are being executed on Github Actions Runner. For Execution we are using Newman,
and htmlextra for Report genration. Using GitHub Action we are able to execute our collection or tests whenever there is push request to the main branch. You can also execute the project with manual runner under the
Actions tab.

Further, the report genrated during the collection run in GitHub Runner memory is archived using upload artifact action in the workflow file. This report file is then displayed with the help of GitHub Pages and then
mailed to the receiver address. We are also using Gmail SMTP for sending E-mails to the recievers. 

## Tech Stack Used ##
1. Postman
2. node.js v22
3. Newman
4. Newman-reprter-htmlextra
5. GitHub Actions
6. Gmail SMTP
7. GitHub Pages
8. AWS EC2 for self hosted runner
9. CSV File for data driven

## GitHub Pages ##
Report genrated with Newman-reporter-htmlextra can be directly viewed over https://vishalxxx.github.io/SDET/ with the help of GitHub Pages.

## How to run the project ##
1. Clone the project on your local machine.
2. Install Node.js ,npm, Newman and NewMan-reporter-htmlExtra
3. Run the project using
 ```
                              newman run in-warrenty-flow.postman_collection.json 
                             -e QA.postman_environment.json 
                             -d testdata.csv 
                             -r cli,htmlextra
```
## Html Report ##
The Report will be created in Newman folder.

## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge Cases Testing
3. Token Testing
4. Data Driven Testing
5. Schema validation
6. Secrets management with GitHub
