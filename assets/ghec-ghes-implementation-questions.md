# GHEC/GHES Implementation and Migration Checklist/Questionnaire

## General GHE Implementation

1.  Have your team attended the GHE Admin workshop/training provided by GitHub or GitHub Partner? When did it happen?
2.  Have your team attended other GHE workshops/trainings provided by GitHub or GitHub Partner? When did it happen?
3.  Do you have GHE Cloud invite? Do you have admin access to GHE Enterprise Account?
4.  Do you have enough license seats for GitHub Enterprise? What is the total number of available license seats?
5.  Have you reviewed and made decisions about GHE implementation with your Enterprise Architecture, Security teams or other stakeholders? If not, what is the timeline to make decisions?
6.  Are there any outstanding issues with GitHub account manager or GitHub support which must be resolved prior to implementation?
7.  What is the preferred method for authentication: GitHub.Com, SSO/SAML with GitHub.Com, Enterprise Managed Users? Which IdP provider you plan to integrate with for authenticating users with GHE?
8.  If chose IdP with EMU, have you received the access to the EMU-enabled GHE Enterprise Account? As of Feb 2023, EMU-enabled GHE account require special provisioning by GitHub and it is separate from the regular GHE Enterprise Account.
9.  Are you planning to set up custom integrations to 3rd party or internal tooling or infrastructure? Describe these services (volume, function, location)
10. Is there a set of branch protections and other repo settings that should be migrated or configured?
11. Do you have a team structure that needs to be brought over or updated/consolidated? E.g. for permission levels for different projects
12. Are you planning to restrict access to GitHub based on IP address for users and integrated applications?
13. Are you planning to set up or require SSH based access?
14. Are you planning to set up 2FA? Any preferred method/app?
15. Are you planning to allow all or some organizations to use GitHub Actions?
16. What are the restrictions to use Actions from Actions Marketplace (All Actions, Actions provided by your enterprise only, Actions from Verified Publishers, Actions from specific publishers)?
17. Are you planning to use DependaBot security alerts?
18. Are you planning to use Advanced Security features? Do you have enough Advanced Security licenses for your users?
19. Are you planning to set up an IP allow list to manage access at enterprise or organizations level?
20. Are you planning to use Self-Hosted Runners for GitHub Actions? What are the preferred environments for hosting runners: Azure, AWS, GCP, other cloud or private/on-prem. Level of familiarity with VM and Container-based/auto-scaling runner implementation.
21. Are you planning to use any GitHub Apps from the marketplace or open sources? If yes, which ones do you plan to use?
22. Are you planning to use Git LFS (large file storage)?
23. Are you planning to use GitHub Container Registry to host Docker images?
24. Are you planning to use GitHub Packages to host nuget, maven, npm packages?
25. Are you planning to use GitHub secrets store? Do you use external secret stores for secrets management? If yes, what are they?
26. Are you planning to integrate a log monitoring tool (i.e. Splunk, DataDog)? Do you plan to configure log streaming to these services or will perform the periodic pull of log data from GitHub API?
27. What are your requirements about log and artifacts retentions policies? Are there any regulatory restrictions? (Maximum is 90 days)
28. Are you planning to use GitHub CodeSpaces?
29. Are you planning to use GitHub Copilot?
30. What are the usage/cost limits are you planning to have in GHE and at what levels (enterprise, organization)? Are you aware of resources available as part of GHE plan and metered resources (e.g. storage, compute minutes) and impact on the GHE cost?
31. What is your current support plan for GHE provide by GitHub (Standard, Premium, Premium Plus)? Are you aware of GitHub support response time/SLA?

## GHES Specific

1.  What is the version of GHE Server? What is the current configuration of underlying VM?
2.  Do you plan for backup and restore of GHES? Do you have sufficient resources?
3.  Do you plan to use disaster recovery strategy for GHES? Do you have resources for standby/passive server node?
4.  Have you run or plan to run the trial disaster recovery scenarios to improve resiliency of GHES? What is the estimated time to restore GHES services in case of failure?

## Migration Specific

1.  Do you need to migrate the work items (e.g. issues, work items, tickets) into GitHub issues or projects?
2.  Do you need to migrate the artifact stores, packages, container registries to GitHub?
3.  Are you planning to migrate repositories to GitHub? Describe them (size, volume) What is the number of repositories and their respective sizes (Mbyte, GByte)? What is the last commit date?
4.  Are you able to identify the repository owners inside your organization? Repository owner can be a physical project team which actively maintains the code in repo.
5.  What version of source system (e.g. SVN, AzDO, GHE Server, BitBucket( are you currently using?
6.  Is the source a SaaS or virtual appliance (e.g. hosted in Azure, AWS, GCP, private data center)? Is the source system working on-premises, cloud infrastructure or provided as a SaaS solution? (e.g. BitBucket Server vs. Cloud, AzDO Server and AzDO Cloud)
7.  Are you using any add-ons or extra tools for source system where you are migrating from? (e.g. security scanning tools, code analysis tools, deployment tools)
8.  Do you need to migrate or update any base access settings or other enterprise and org settings?
9.  Are you planning to migrate webhooks set up in GitHub Enterprise?
10. Do you want to consolidate organizations to allow for more collaboration?
