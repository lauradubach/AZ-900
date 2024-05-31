# Describe Azure Virtual Machines

Azure Virtual Machines (VMs) provide cloud-based virtualized servers, offering Infrastructure as a Service (IaaS) with customizable software and operating system options. They allow total control over the OS, the ability to run custom software, and accommodate custom hosting configurations. Azure VMs offer flexibility without the need to manage physical hardware directly, but users are still responsible for configuring and maintaining the software.
You can quickly provision VMs using preconfigured images, which serve as templates and can include an OS and other necessary software. Azure offers options to scale VMs, either individually for testing or in groups for high availability and scalability. Virtual machine scale sets automate the management of identical, load-balanced VM groups, adjusting instance counts based on demand. Availability sets ensure VM resilience by distributing them across update and fault domains to mitigate failures.
Common use cases for Azure VMs include testing and development, running applications in the cloud, extending on-premises networks, and disaster recovery. VMs are also suitable for migrating physical servers to the cloud with minimal changes. When provisioning a VM, users can select resources such as size (CPU cores, RAM), storage disks, and networking configurations.

# Describe Azure Virtual Desktop

Azure Virtual Desktop is a cloud-based desktop and application virtualization service offered by Azure. It provides users with access to a cloud-hosted version of Windows from anywhere, on various devices and operating systems. Users can access their virtual desktops and applications through remote desktop apps or modern browsers.
Security is enhanced through centralized management with Microsoft Enterprise ID and support for multifactor authentication. Granular role-based access controls (RBACs) ensure secure data access.
Data and applications are hosted in the cloud, reducing the risk of data exposure on personal devices. User sessions are isolated, maintaining security in both single and multi-session environments.
Azure Virtual Desktop supports multi-session deployments of Windows 10 or Windows 11 Enterprise, offering a consistent experience with broader application support compared to Windows Server-based systems.

# Describe Azure Containers

Azure containers offer a lightweight virtualization environment that enables running multiple instances of an application on a single host machine. Unlike virtual machines, containers do not require managing the operating system individually. They are agile, scalable, and designed to respond to changes dynamically, with Docker being a popular container engine supported by Azure.
Azure provides several container services:

1. Azure Container Instances (ACI): A platform as a service (PaaS) offering that simplifies container deployment without managing virtual machines. ACI allows users to upload containers and run them directly on the service.
2. Azure Container Apps: Similar to ACI, Container Apps streamline container management and offer additional features like load balancing and scaling for enhanced elasticity in design.
3. Azure Kubernetes Service (AKS): A container orchestration service that simplifies container fleet management. AKS manages the lifecycle of containers and provides efficient deployment and scaling capabilities.
Containers are commonly used in microservice architectures, where solutions are broken into smaller, independent components. For instance, a website might be split into containers for front-end, back-end, and storage, allowing independent maintenance, scaling, or updates. Containers enable flexible scaling of specific components, enhancing performance without impacting other parts of the solution.


# Describe Azure Functions

Azure Functions is a serverless compute option in Azure, operating without the need for managing virtual machines or containers. Instead of keeping resources running continuously, Functions are triggered by events, ensuring efficient resource allocation.
Key points about Azure Functions:
1. Event-driven and serverless: Azure Functions respond to events, such as REST requests, timers, or messages from other Azure services, without the need for continuous resource provisioning.
2. Benefits: Functions are ideal when the focus is solely on the code, without concern for underlying infrastructure. They automatically scale based on demand and are suitable for workloads that can be completed quickly, within seconds or less.
3. Automatic scaling and cost-efficiency: Functions scale automatically based on demand, ensuring optimal resource utilization. Users are only charged for CPU time while the function is running.
4. Stateful or stateless: Functions can be stateless (default), where they restart with each event, or stateful (Durable Functions), which track prior activity through a context.
5. Flexibility: Azure Functions offer flexibility to deploy projects in both serverless and non-serverless environments. This enables managing scaling, running on virtual networks, or complete function isolation based on changing app needs.
Azure Functions are a fundamental component of serverless computing, providing a versatile compute platform for various types of code, with the ability to adapt to evolving application requirements.

# Describe application hosting options

Azure offers various hosting options for applications, including virtual machines (VMs), containers, and Azure App Service.
Virtual Machines (VMs) and Containers:

- VMs provide maximum control over the hosting environment, allowing customized configurations.
- Containers offer robust hosting by isolating and managing different aspects of the solution.
- Both options are excellent choices for hosting applications on Azure.
    
### Azure App Service
1. App Service enables hosting of web apps, background jobs, mobile back-ends, and RESTful APIs without managing infrastructure.
2. It supports automatic scaling, high availability, and deployment automation from GitHub, Azure DevOps, or Git repos.
3. App Service supports multiple languages and environments, including Windows and Linux.
    
### Types of App Services
1. Web Apps: Supports various languages and frameworks like ASP.NET, ASP.NET Core, Java, Ruby, Node.js, PHP, or Python, on both Windows and Linux.
2. API Apps: Enables building REST-based web APIs with Swagger support, consumable by any HTTP/HTTPS client.
3. WebJobs: Runs programs or scripts in the context of web, API, or mobile apps, commonly used for background tasks.
4. Mobile Apps: Quickly builds back ends for iOS and Android apps, with features like cloud-based SQL database storage, social authentication, push notifications, and custom logic execution in C# or Node.js.
5. Azure App Service simplifies infrastructure management, allowing developers to focus on building and maintaining applications while Azure ensures the environment's uptime and scalability.

# Describe Azure virtual network

Azure virtual networks and virtual subnets facilitate communication between Azure resources, including VMs, web apps, and databases, as well as with on-premises client computers and the internet. Key capabilities include isolation, segmentation, routing, and traffic filtering.

Key Networking Capabilities:
1. Isolation and Segmentation:Azure virtual networks create isolated networks with defined private IP address spaces, divided into subnets.
2. Internet Communications:Resources can communicate with the internet via public IP addresses or public load balancers.
3.Communicate Between Azure Resources:Virtual networks connect various Azure resources, including VMs, App Service Environment, Azure Kubernetes Service, and virtual machine scale sets. Service endpoints link Azure SQL databases and storage accounts to virtual networks.
4. Communicate with On-Premises Resources: Connectivity options include point-to-site VPN connections, site-to-site VPN connections, and Azure ExpressRoute for dedicated private connectivity.
5. Route Network Traffic: Route tables and Border Gateway Protocol (BGP) enable traffic routing between subnets and on-premises networks.
6. Filter Network Traffic:Network security groups and network virtual appliances provide inbound and outbound traffic filtering based on rules and protocols.
7. Connect Virtual Networks:Virtual network peering allows direct connectivity between virtual networks, enabling private communication across regions. User-defined routes offer control over traffic flow within or between virtual networks.

# Describe Azure virtual private network

A virtual private network (VPN) establishes an encrypted tunnel within a network, commonly used to connect trusted private networks over untrusted networks like the internet. VPNs ensure secure communication by encrypting traffic to prevent eavesdropping or attacks, facilitating safe sharing of sensitive information.

### Azure VPN Gateways:
- Azure VPN Gateway instances, deployed within a dedicated subnet of a virtual network, enable various connectivity options:
  - Site-to-site connections: Connect on-premises datacenters to virtual networks.
  - Point-to-site connections: Connect individual devices to virtual networks.
  - Network-to-network connections: Connect virtual networks to other virtual networks.
- All data transmission is encrypted within a private tunnel over the internet.
- Each virtual network supports one VPN gateway, which can connect to multiple locations, including other virtual networks or on-premises datacenters.

### Types of VPNs:
- Policy-based VPN Gateways: Determine encrypted traffic based on statically specified IP addresses.
- Route-based VPN Gateways: Use IP routing to determine which tunnel interface to use for each packet, offering greater resilience to topology changes.

### Maximizing VPN Gateway Resiliency:
- Active/Standby Configuration: Default deployment with two instances, ensuring failover without user intervention during maintenance or disruptions.
- Active/Active Configuration: Utilize support for BGP routing protocol, assigning unique public IP addresses to each instance, and creating separate tunnels for each on-premises device.
- ExpressRoute Failover: Configure VPN gateway as a secure failover path for ExpressRoute connections to ensure connectivity during ExpressRoute disruptions.
- Zone-Redundant Gateways: Deploy gateways in Azure availability zones for enhanced resiliency, scalability, and availability, using Standard public IP addresses and distinct gateway SKUs.

# Describe Azure ExpressRoute

Azure ExpressRoute allows organizations to extend their on-premises networks to the Microsoft cloud via a private connection provided by a connectivity provider, establishing ExpressRoute circuits. This enables direct connectivity to Microsoft cloud services such as Azure and Microsoft 365, enhancing connectivity, reliability, speed, latency consistency, and security compared to typical internet connections.

### Key Features and Benefits:
1. Connectivity to Microsoft Cloud Services: Access Azure services, Office 365, Dynamics 365, and other Microsoft cloud services globally.
2. Global Connectivity: Utilize ExpressRoute Global Reach to exchange data between on-premises sites connected by ExpressRoute circuits.
3. Dynamic Routing: Exchange routes between on-premises networks and Azure using Border Gateway Protocol (BGP) for dynamic routing.
4. Built-in Redundancy: Ensure high availability with redundant devices deployed by connectivity providers.
5. Security Considerations: Transmit data securely over the private connection, avoiding exposure to risks associated with the public internet.

### ExpressRoute Connectivity Models:
1. CloudExchange Colocation: Co-locate your facility at a cloud exchange and request a virtual cross-connect to the Microsoft cloud.
2. Point-to-Point Ethernet Connection: Establish a point-to-point connection between your facility and the Microsoft cloud.
3. Any-to-Any Networks: Integrate your wide area network (WAN) with Azure, connecting offices and datacenters.
4. Directly from ExpressRoute Sites: Connect directly to Microsoft's global network at strategically distributed peering locations, with ExpressRoute Direct offering high-speed connectivity options.

ExpressRoute ensures private connectivity, protecting data from potential internet-related risks. Despite ExpressRoute's private nature, certain communications like DNS queries and Azure Content Delivery Network requests still traverse the public internet.

#Describe Azure DNS

Azure DNS is a Microsoft Azure service offering domain name hosting, enabling name resolution through Azure infrastructure. Hosting domains in Azure allows unified management of DNS records alongside other Azure services, using the same credentials, APIs, tools, and billing.

### Benefits of Azure DNS:
1. Reliability and Performance: Hosted on Azure's global network of DNS name servers, leveraging anycast networking for resiliency and high availability, ensuring fast performance.
2. Security: Based on Azure Resource Manager, offering Azure RBAC for access control, activity logs for monitoring, and resource locking to prevent accidental modifications.
3. Ease of Use:* Integrated into the Azure portal, supporting management via Azure PowerShell cmdlets, Azure CLI, REST API, and SDKs, facilitating automated DNS management.
4. Customizable Virtual Networks: Supports private DNS domains, allowing custom domain names in private virtual networks.
5. Alias Records: Supports alias record sets, enabling referencing of Azure resources like public IP addresses, Traffic Manager profiles, or CDN endpoints, with automatic updates during IP address changes.

### Important Note:
Azure DNS does not facilitate domain name purchasing. Domains can be acquired through services like App Service domains or third-party registrars and then hosted in Azure DNS for record management.

