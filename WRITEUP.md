# Write-up : Deploy An Article CMS to Azure

## Andrew GE

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*

- *Analyze costs, scalability, availability, and workflow*
> **VM**: providing infrastructure as a service (IaaS) by allowing you to create and use virtual machines in the cloud.
- For VM solution, user do not need to purchase and maintain the hardware which lower the cost. 
- VMs are highly scalabile and flexible to configure. Users will have full access and control of the VM. The VMs can be grouped to provide high availability. 
- The CPU, memories and other resouces can be optimzed to fit the need.  As the demands changing, the VMs can be scaled up or down.
- As user has full control of the VM, all the OS, software packages and applications must be installed and maintained by the user.
- To deploy a web severvice, one need to initiate the VM, install the OS, put the software development packeages and actually using scripts or other means to start the web service.

> **App Service**: Azure App Service is a Platform as a Service (PaaS). It is an HTTP-based service for hosting web applications, REST APIs, and mobile back ends.
In this case the cloud provider,Azure, takes care of the infrastructure.
 
- Azure web service provide the flexible cost structure for appropriate hardware allocation to host the application. The cost is based on the plan selected.
- As stated in the NanoDegree lession, the Azure app service is Vertical or Horizontal scaling: _"Vertical scaling increases or decreases resources allocated to our App Service, 
such as the amount of vCPUs or RAM, by changing the App Service pricing tier. Horizontal scaling increases or decreases the number of Virtual Machine instances our App Service is running."_
- App service is deployed in the Azure cloud, it has high availability with local and geo-redundency.
- The app service can be deployed with automatic models, i.e., GitHub. 
- As the PaaS nature, the app service limit the access to underline OS and software package. User has to pay for the service plan, even if your services or application isn’t running.
There are hardware limitations, such as a maximum of 14GB of memory and 4 vCPU cores per instance.

- *Choose the appropriate solution (VM or App Service) for deploying the app*:

> In this project, I am chosing the **App Service** for deploying the app.
 
- *Justify your choice*

> For this project, the resource required is very limited. There is no chance to cross the upper limit of the app service provided. There are not special features that requiring the 
access of the OS and other specific software packet for this project. We do not need to install the OS and many supporting software packages. In addition, we are using Python with is a suported
language for the app service. This makes the deployment simple. In addtion, we can fork the Git from the provided template and develop features on top of it. From the cost point of view, the 
number of transcations and amount of CPU/memory are very limited. We can use the free plan for this App Service. 


### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 