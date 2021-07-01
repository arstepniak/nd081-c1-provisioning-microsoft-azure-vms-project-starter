# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*


VM and App Service both provide the ability to host web application on Azure. The first one is offered as IaaS, providing a machine which needs to be maintained by the machine creator. The costs are higher compared to the App Service but the solution offers more control over the application host. Unfortunately setting up the VM to host application is definitly more time consuming than using the App Service.
The App Service is the solution that offers hosting web application using PaaS model. We have no access to the host server, but it allows developer to focus more on the application development than on setting up the machine. One major disadvantage is that we're always paying for the App Service until we delete/suspend it. Another flaw to mention is that the deployment is limited only to few languages, including Python, PHP, .NET etc. Good thing about this solution is that you can set a CI/CD pipeline using, for example, a GitHub repository - it allows quick changes to the application as needed.

After the analysis I'd choose App Service to host the application. It's because App Service offers more flexibility regarding CI/CD and it's very easy to setup. For the first app deployment it's good to test out and see what network traffic we would get. We can also focus more on app development than taking care over VM maintenance, updates etc.

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

I'd change the decision when the app would receive more network traffic and the number of app's features would increase in numbers. I'd migrate it to the VM in order to have more control over the host server and to have more scalability regarding the hardware I can choose, compared to the App Service.
