# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

## Analyze costs
### VM
- Lower up-front cost compared to purchasing and maintaining hardware.
- Multiple types to choose from, such as compute or memory-optimized VMs, along with varying amounts of CPU, RAM, and storage.
- Lightweight API, tiny web/application will not need VM because CMS app very tiny.
### App Service
- Always paying for the service plan, even if your services or application isn’t running.
- CMS app to only practice to upload app to Azure, So I thinks I will use dev/test app servicev for App Service

## Scalability
### VM
- Virtual Machine Scale Sets and Load Balancers
- Multiple types to choose from, such as compute or memory-optimized VMs, along with varying amounts of CPU, RAM, and storage.
-> CMS no need

### App Service
- There are hardware limitations, such as a maximum of 14GB of memory and 4 vCPU cores per instance
- They are limited to just using those languages
- Vertical or Horizontal scaling. Vertical scaling increases or decreases resources allocated to our App Service, such as the amount of vCPUs or RAM, by changing the App Service pricing tier. Horizontal scaling increases or decreases the number of Virtual Machine instances our App Service is running.
-> CMS no need Scalability, and only using python 3.7 ++ , 

## Availability
### VM
-  Multiple VMs can be grouped to provide high availability, scalability, and redundancy.
### App Service
- High availability, auto-scaling, and support of both Linux and Windows environments.
 VM and App Service are  high availability

## Workflow
### VM
- They can be more time consuming for the developer than other compute options
- Need install nginx, python3.7 ++, sql driver, Flask, azure-nspkg, azure-common....  and more libraries
- Need config nginx and more
### App Service
- Only care to source code and call API from libraries, e.x: MSAL, no need install sql driver, and many config .....


-> I will using App Service for CMS app
Cause: 
   Workflow: faster and no need care any library
   Analyze costs: This is tiny app, so I think it cheaper than VM

My link Python App Service
https://articlecsm-sonnt2.azurewebsites.net/

