#### Getting started
* Example walkthrough [here](https://raw.githubusercontent.com/6869736572/open-notes/master/Cloud/Chef/First%20Steps/Example.txt)

* Plan your environment: Will you run the solution locally or on a cloud vendor such as AWS, Azure, or GCP? This decision will determine how you execute the installation and configuration steps (below).

* Install and configure Chef: There is no better documentation on installing and configuring software than from the vendor themselves. Follow the steps [here](https://docs.chef.io/workstation/install_workstation/) according to the OS your host runs on.

* Install and configure Test Kitchen: Good news, batteries are included! If you've installed Chef Workstation, Test Kitchen now comes included.

* Install and configure Vagrant: Using VirtualBox+Vagrant is optional. For example, if you are running on AWS, Azure, or GCP, you don't need Vagrant. Follow the steps [here](https://www.vagrantup.com/docs/installation) to install and configure Vagrant.

* Deploy your nodes: If you have not already deployed nodes while going through your course material, do so now. You can use the "Get started" tutorial at learn.chef.io to deploy an Ubuntu node on either Vagrant (local), AWS, or Azure.

* Go through the normal kitchen list / kitchen create / kitchen converge workflow. If you are unsure of how to do this, it's the exact flow you learned in the above tutorial at learn.chef.io.

* Note: The default.rb recipe is simply an Apache web server, which will be fine for demonstration purposes.

* At this point, your nodes should be operational. Now, we should turn our attention to log collection and systerm performance monitoring. We can do this in a few ways (scripts, local agents, etc.)...


#### You can communicate with your nodes in a number of ways:
* AWS/Azure/GCP: Use the corresponding CLI, API, and SSH.
* Vagrant: Access your machines through Vagrant. "vagrant global-status" --> "vagrant ssh node-id" --> "vagrant/vagrant" --> "top"
* Chef: Use "kitchen exec" to run commands on the remote node.
