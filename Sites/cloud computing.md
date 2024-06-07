# What is Cloud Computing

Cloud computing is the delivery of computing services over the internet. Computing services include common IT infrastructure such as virtual machines, storage, databases, and networking. Cloud services also expand the traditional IT offerings to include things like Internet of Things (IoT), machine learning (ML), and artificial intelligence (AI).
Because cloud computing uses the internet to deliver these services, it doesn’t have to be constrained by physical infrastructure the same way that a traditional datacenter is. That means if you need to increase your IT infrastructure rapidly, you don’t have to wait to build a new datacenter you can use the cloud to rapidly expand your IT footprint.

# Shared Responsibility Model

![Responsibility model](<../Pictures/Responsibility Model.png>)

When using a cloud provider, you’ll always be responsible for:
- The information and data stored in the cloud
- Devices that are allowed to connect to your cloud (cell phones, computers, and so on)
- The accounts and identities of the people, services, and devices within your organization

The cloud provider is always responsible for:
- The physical datacenter
- The physical network
- The physical hosts

Your service model will determine responsibility for things like:
- Operating systems
- Network controls
- Applications
- Identity and infrastructure

## IAAS
You’re responsible for everything else: operating system installation, configuration, and maintenance; network configuration; database and storage configuration.

The cloud provider is responsible for maintaining the physical infrastructure and its access to the internet. You’re responsible for installation and configuration, patching and updates, and security.

### Some common scenarios where IaaS might make sense include:
- Lift-and-shift migration: You’re setting up cloud resources similar to your on-prem datacenter, and then simply moving the things running on-prem to running on the IaaS infrastructure.
- Testing and development: You have established configurations for development and test environments that you need to rapidly replicate. You can start up or shut down the different environments rapidly with an IaaS structure, while maintaining complete control.

## PAAS

Platform as a service (PaaS) is a middle ground between renting space in a datacenter (infrastructure as a service) and paying for a complete and deployed solution.

The cloud provider is responsible for maintaining the physical infrastructure and its access to the internet, just like in IaaS. In the PaaS model, the cloud provider will also maintain the operating systems, databases, and development tools

### Some common scenarios where PaaS might make sense include:
- Development framework: PaaS provides a framework that developers can build upon to develop or customize cloud-based applications. Similar to the way you create an Excel macro, PaaS lets developers create applications using built-in software components. Cloud features such as scalability, high-availability, and multi-tenant capability are included, reducing the amount of coding that developers must do.
- Analytics or business intelligence: Tools provided as a service with PaaS allow organizations to analyze and mine their data, finding insights and patterns and predicting outcomes to improve forecasting, product design decisions, investment returns, and other business decisions.

## SAAS
With SaaS, you’re essentially renting or using a fully developed application. Email, financial software, messaging applications, and connectivity software are all common examples of a SaaS implementation.

SaaS is the model that places the most responsibility with the cloud provider and the least responsibility with the user. In a SaaS environment you’re responsible for the data that you put into the system, the devices that you allow to connect to the system, and the users that have access.

The cloud provider is responsible for physical security of the datacenters, power, network connectivity, and application development and patching.

### Some common scenarios for SaaS are:
- Email and messaging.
- Business productivity applications.
- Finance and expense tracking.

# Cloud Modules

![Cloud Modules](<../Pictures/Cloud Modules.png>)

# Multicloud
In a nutshell, a multi-cloud scenario involves utilizing multiple public cloud providers simultaneously. This could be due to leveraging different features from various providers or transitioning from one provider to another. In a multi-cloud environment, managing resources and security involves overseeing operations across two or more cloud platforms.
 
# Azure Arc:
Azure Arc is a set of technologies that helps manage your cloud environment. Azure Arc can help manage your cloud environment, whether it's a public cloud solely on Azure, a private cloud in your datacenter, a hybrid configuration, or even a multi-cloud environment running on multiple cloud providers at once.
 
# Consumption based Model
 
When comparing IT infrastructure models, there are two main types of expenses: Capital Expenditure (CapEx) and Operational Expenditure (OpEx).
1. CapEx involves one-time, upfront costs for tangible resources like building construction, data center establishment, or vehicle purchase.
2. OpEx encompasses ongoing expenses for services or products over time, such as renting a venue, leasing vehicles, or subscribing to cloud services.

Cloud computing is categorized under OpEx because it operates on a consumption-based model. Rather than paying for physical infrastructure and associated maintenance costs, users pay only for the IT resources they utilize. This model offers benefits like:
- No upfront costs.
- No need to invest in and manage potentially underutilized infrastructure.
- Flexibility to scale resources up or down as needed.
- Ability to stop paying for unused resources.

In contrast, traditional data centers require estimating future resource needs, which can lead to either over-provisioning (wasting money) or under-provisioning (resulting in decreased performance and lengthy fixes). With cloud-based models, users can dynamically adjust resources without worrying about excess capacity, ensuring efficient resource utilization and cost savings.
 
# Cloud Pricing Models
 
Cloud computing is a service delivery model over the internet, offering a pay-as-you-go pricing structure. Users pay for the specific cloud services they use, leading to:
- Efficient planning and management of operating costs.
- Enhanced infrastructure operation efficiency.
- Flexibility to scale resources based on business requirements.

In essence, cloud computing involves renting compute power and storage from remote data centers, akin to managing resources in your own data center. However, unlike traditional setups, users return cloud resources when no longer needed and are billed solely for their usage. This arrangement eliminates the need to maintain physical infrastructure, as the cloud provider handles maintenance. Ultimately, cloud computing empowers businesses to tackle challenges swiftly and deliver innovative solutions to their users.

