# DevOps improvements :
* AWS Account Segregation for PROD and Non-Prod environments/stack
* Setup CI/CD pipelines with gitlab workflow integration as separate deployables (I’d recommend to go with AWS CDK as IaC framework -  TBD or else we may go with Terraform )
* Create Seperate Slack channels and Prod and Non-Prod Release/Deployments and integrate CI/CD setup for push prod/non-prod deployment notifications
* Setup and configure Monitoring / alerting tools for production and sandbox - (Grafana + cloudwatch metrics + Slack  - TBD)
* Setup proper log analysis mechanism for troubleshooting  (we may use ELK or EKK stack- TBD)
* Introdroduce Feature Flagging concept to the platform since it would be very useful in future feature Development/Releasing/Maintenance handling etc.. (example tool : LaunchDarkly  https://launchdarkly.com/)
* Setup and configure E2E framework(eg: cucumber ) and integrate it with CI/CD workflow
* Setup and configure Performance Testing framework/tool for getting benchmark statistics and this can be also integrated with CI/CD flow (eg : Grafana K6 https://k6.io/docs/ )
* Setup and configure incident management system for L2 support (eg : https://www.pagerduty.com/)


# Engineering Process improvements:
			
* Setup Release calendar for all planned releases for the entire Quarter or Year.(this can be implemented only once we start sprint based development cycle)
* Introduce ADR process (Architecture Decision Records) across all engineering squads.
* Keep an engineering maturity tracker  eg : https://docs.google.com/spreadsheets/d/1hv-iRt-3qw95d0TTCrfzu7yNuSVPYpvIIZqMC1kq81Q/edit#gid=0
* Setup and define proper Release Management protocol/process across all squads
* Need to Setup and follow for a proper branching  strategy in the for the Gitlab CI
* Integrate ClickUp with GitLab for keeping track of MR/branch for the respective tickets (also we would need to follow proper naming conventions for branching https://help.clickup.com/hc/en-us/articles/6305774858263-GitLab
* Move API collection to a Postman Team workspace rather than keeping a stand alone collection with individuals , this will help full squad to keep API collection up to date and working on a shared collection . I have already moved it to the teamspace in the free tire
https://almondfintech.postman.co/workspace/Team-Workspace~8aca7eb0-feab-4222-8179-370646bbf913/collection/25377604-f93ba10d-4a14-4da5-b397-ff9a928506a1?ctx=documentation

# Architectural and Code level Improvements :

* Increase Unit Testing Coverage of the all repositories and configure coverage rule with CI/CD setup (eg : at least 80% of new code should covered by unit testing )
* Start writing E2E Testing scenarios for all API Endpoints.
* Keep all AWS Network/Component diagrams up-to date with correct service/component names
* Would be great if we can have a master diagram of technical architecture.
* Update ReadMe Docs for all repositories with all necessary information, this would be really helpful for onboarding new engineers.
* Application logs needs to be improved across all services/components since current logging steps are not sufficient for end to end troubleshooting , eg : needs to be add more Info Level logs for each step or method calling 
* Introduce mutation testing - only if its necessary