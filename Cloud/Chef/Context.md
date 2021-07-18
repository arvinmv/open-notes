### Some resources
```   
● Learn Chef (learn.chef.io)
---- Chef101 Beginning your Chef journey
---- Infra101 Manage your fleet with Chef Infra
---- Git101 Getting started with git
---- LocalDev101 Validate infrastructure code with Test Kitchen (Optional)
● Text: "Chef: Powerful Infrastructure Automation (At least Module 2)"
● Pluralsight: "Getting Started with Chef Fluency"
```

### Some quick context
You may understand the operational need to automate deployments and scale infrastructure. But how is this accomplished? The approach and tools can take many forms, but eventually you (or your organization) will standardize over particular processes, services, and tools. You may recall that the AWS Well-Architected Framework defines five pillars to be considered during cloud operations: operational excellence, security, reliability, performance efficiency, and cost optimization. Many of these goals are realized by implementing the following:
```
--Version control your infrastructure and deploy it from code
--Identify bottlenecks, then reduce requests (reads/writes) by caching where it makes sense
--Design loosely coupled systems and design stateless servers (serverless, containers, microservices, etc.)
--Scale and load balance wisely (autoscaling, horizontal, vertical, auto, etc.)
--Test your systems (chaos engineering)
```
Each of these approaches are relevant to using Chef *well*.


#### What is configuration management?
Configuration management is a process for maintaining computer systems, servers, and software in a desired, consistent state. It’s a way to make sure that a system performs as it’s expected to as changes are made over time. Managing IT system configurations involves defining a system's desired state—like server configuration—then building and maintaining those systems. Closely related to configuration assessments and drift analyses, configuration management uses both to identify systems to update, reconfigure, or patch.


#### Why manage configurations?
Configuration management keeps you from making small or large changes that go undocumented. These misconfigurations can lead to poor performance, inconsistencies, or noncompliance and negatively impact business operations and security. When undocumented changes are made across many systems and applications, it adds to instability and downtime. 

Manually identifying systems that require attention, determining remediation steps, prioritizing actions, and validating completion are too complicated to perform in large environments. But without documentation, maintenance, and a change control process, system administrators and software developers could end up not knowing what’s on a server or which software has been updated. Configuration management systems let you consistently define system settings, as well as build and maintain those systems according to those baseline settings. Configuration management helps users and administrators know where certain services exist and what the current state of applications are.

Proper configuration management tools:
``` Classify and manage systems by groups and subgroups. 
Centrally modify base configurations.
Roll out new settings to all applicable systems. 
Automate system identification, patches, and updates
Identify outdated, poor performing, and noncompliant configurations. 
Prioritize actions. 
Access and apply prescriptive remediation.
```


#### Configuration management benefits
Think of it like this. If you keep up with the small things, you can avoid more complicated, expensive repairs in the future. Configuration management is about preventing issues so you don’t have to deal with as many problems later.  For example, you can make sure that your test and production environments match. That way, you’ll have fewer problems with applications once they’ve been deployed than you would if these environments weren’t exactly the same. With configuration management, you can accurately replicate an environment with the correct configurations and software because you know what exists in the original environment.


#### Automating configuration management
The role of configuration management is to maintain systems in a desired state. Traditionally, this was handled manually or with custom scripting by system administrators. Automation is the use of software to perform tasks, such as configuration management, in order to reduce cost, complexity, and errors. Through automation, a configuration management tool can provision a new server within minutes with less room for error. You can also use automation to maintain a server in the desired state, such as your standard operating environment (SOE), without the provisioning scripts needed previously.


Source: https://www.redhat.com/en/topics/automation/what-is-configuration-management


#### What is Infrastructure as Code (IaC)?
Infrastructure as Code (IaC) is the managing and provisioning of infrastructure through code instead of through manual processes. With IaC, configuration files are created that contain your infrastructure specifications, which makes it easier to edit and distribute configurations. It also ensures that you provision the same environment every time. By codifying and documenting your configuration specifications, IaC aids configuration management and helps you to avoid undocumented, ad-hoc configuration changes. Version control is an important part of IaC, and your configuration files should be under source control just like any other software source code file. 

Deploying your infrastructure as code also means that you can divide your infrastructure into modular components that can then be combined in different ways through automation. Automating infrastructure provisioning with IaC means that developers don’t need to manually provision and manage servers, operating systems, storage, and other infrastructure components each time they develop or deploy an application. 

Codifying your infrastructure gives you a template to follow for provisioning, and although this can still be accomplished manually, an automation tool, such as Red Hat® Ansible Automation® Platform, can do it for you. With Ansible Automation Platform, playbooks are used to describe the desired state of your infrastructure, which the tool can then provision. You can also use Ansible Automation Platform for configuration management to maintain your systems in the desired state.
 
 
#### Declarative vs. imperative approaches to IaC
There are 2 ways to approach IaC—declarative or imperative. A declarative approach defines the desired state of the system, including what resources you need and any properties they should have, and an IaC tool will configure it for you. A declarative approach also keeps a list of the current state of your system objects, which makes taking down the infrastructure simpler to manage.

An imperative approach instead defines the specific commands needed to achieve the desired configuration, and those commands then need to be executed in the correct order. Many IaC tools use a declarative approach and will automatically provision the desired infrastructure. If you make changes to the desired state, a declarative IaC tool will apply those changes for you. An imperative tool will require you to figure out how those changes should be applied.

IaC tools are often able to operate in both approaches, but tend to prefer 1 approach over the other.


#### Benefits of IaC
Provisioning infrastructure has historically been a time consuming and costly manual process. Now infrastructure management has moved away from physical hardware in data centers, though this still may be a component for your organization, to virtualization, containers, and cloud computing. With cloud computing, the number of infrastructure components has grown, more applications are being released to production on a daily basis, and infrastructure needs to be able to be spun up, scaled, and taken down frequently. Without an IaC practice in place, it becomes increasingly difficult to manage the scale of today’s infrastructure.

IaC can help your organization manage IT infrastructure needs while also improving consistency and reducing errors and manual configuration. Benefits:
```
Cost reduction
Increase in speed of deployments
Reduce errors 
Improve infrastructure consistency
Eliminate configuration drift
IaC tool examples


```
Server automation and configuration management tools can often be used to achieve IaC. There are also solutions specifically for IaC. These are a few popular choices:
```
Chef
Puppet
Red Hat Ansible Automation Platform
Saltstack
Terraform 
AWS CloudFormation
```


Source: https://www.redhat.com/en/topics/automation/what-is-infrastructure-as-code-iac


#### What is orchestration? 
Orchestration is the automated configuration, management, and coordination of computer systems, applications, and services. Orchestration helps IT to more easily manage complex tasks and workflows. IT teams must manage many servers and applications, but doing so manually isn’t a scalable strategy. The more complex an IT system, the more complex managing all the moving parts can become. The need to combine multiple automated tasks and their configurations across groups of systems or machines increases. That’s where orchestration can help.

Automation and orchestration are different, but related concepts. Automation helps make your business more efficient by reducing or replacing human interaction with IT systems and instead using software to perform tasks in order to reduce cost, complexity, and errors. In general, automation refers to automating a single task. This is different from orchestration, which is how you can automate a process or workflow that involves many steps across multiple disparate systems. When you start by building automation into your processes, you can then orchestrate them to run automatically. 

IT orchestration also helps you to streamline and optimize frequently occurring processes and workflows, which can support a DevOps approach and help your team deploy applications more quickly. You can use orchestration to automate IT processes such as server provisioning, incident management, cloud orchestration, database management, application orchestration, and many other tasks and workflows.


#### Orchestration tools
In system administration, orchestration is the automated configuration, coordination, and management of computer systems and software. A number of tools exist for automation of server configuration and management, including Ansible, Puppet, Salt, Terraform, and AWS CloudFormation. Orchestration is often discussed in the context of service-oriented architecture, virtualization, provisioning, converged infrastructure and dynamic datacenter topics. Orchestration in this sense is about aligning the business request with the applications, data, and infrastructure. In the context of cloud computing, the main difference between workflow automation and orchestration is that workflows are processed and completed as processes within a single domain for automation purposes, whereas orchestration includes a workflow and provides a directed action towards larger goals and objectives. In this context, and with the overall aim to achieve specific goals and objectives (described through quality of service parameters), for example, meet application performance goals using minimized costand maximize application performance within budget constraint.

Source: https://en.wikipedia.org/wiki/Orchestration_(computing)
