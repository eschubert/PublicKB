{{{
  "title": "Getting started with Commvault Storage Blueprint",
  "date": "8-31-2015",
  "author": "Bob Stolzberg",
  "attachments": [],
  "contentIsHTML": false
}}}

![Commvault logo](http://webdocs.commvault.com/images/fy15-cio-awareness/cv-stacked.png)

### Partner Profile
Commvault - "Protect, Access, Comply, Share"

[http://www.Commvault.com](http://www.Commvault.com)

#### Contact Commvault   
##### Commvault Support:
24x7 Web Support - [https://www.Commvault.com/](https://www.Commvault.com/)
Email Support - [support@commvault.com](mailto:support@commvault.com)
Phone Support - Call (877) 780-3077

### Description 
Commvault Systems has integrated their technology with the CenturyLink Cloud platform.  The purpose of this KB article is to help the reader take advantage of this integration to achieve rapid time-to-value for this Data Management solution.

Technology from Commvault Systems helps CenturyLink Cloud customers address the business challenge of data protection and data growth by implementing Commvault's Simpana data management solution - now available as part of the CenturyLink Cloud Blueprint Engine.

### Solution Overview
CommVault's holistic approach to cloud management allows you to manage your virtual infrastructure seamlessly across multiple hypervisors and cloud platforms — and to automate and streamline operations over the entire VM lifecycle, from provisioning to protection to decommissioning.

The CommVault Simpana Blueprints offer different ways to manage data in, from and to the CenturyLink Cloud as well as integrate with multiple remote data centers and cloud platforms.  

The 'All in One' Blueprint includes a Windows 2012 Server image with the Simpana components to build out a new CommCell and/or attache to an existing Commcell.  The image has the CommmServe and Media Agent software component ready to be configured as needed for your desired use case.

### Offer
Commvault is making their technology available for CenturyLink Cloud Users to deploy to their account.  Installation of the Commvault Server and All In One Blueprints includes a license good for one month (depending on the actual date of deployment). In order to purchase a license or entitlement, please contact [Contact Commvault sales](http://www.commvault.com/contact-us)

### Audience
CenturyLink Cloud Users and Commvault Simpana customers.

### Impact
After reading this article, the user should feel comfortable getting started using the Commvault technology on CenturyLink Cloud.

After executing the steps in this Getting Started document, the users will have a functioning Commvault Simpana data management platform upon which they can start developing data management solutions.

### Prerequisite
- Access to the CenturyLink Cloud platform as an authorized user.
- Commvault software license

### Postrequisite
- After the Blueprint completes, you will need to RDP to the server, login to the Commvault GUI and perform the follows tasks under Library and Drive configuration, and perform the following taks:
  * Change your default admin password to something secure
  * [Install the Commvault Media Agent](http://documentation.commvault.com/commvault/v10/article?p=deployment.html) on this server
  * [Configure the Commvault libraries](http://documentation.commvault.com/commvault/v10/article?p=features/library_drive_config/library_drive_configuration_getting_started.html) 
  * [Create a schedule policy](http://documentation.commvault.com/commvault/v10/article?p=features/schedule_policy/getting_started.htm) 
  * [Create a deduplication policy](http://documentation.commvault.com/commvault/v10/article?p=features/deduplication/t_creating_a_global_deduplication_policy.htm)

- If you want to access Commvault server over the internet, please perform the following tasks once you receive an email confirming you Blueprint completed successfully:

1. To connect to your Commvault server via the Internet, Add a [Public IP](../../Network/how-to-add-public-ip-to-virtual-machine.md) to your server through Control Portal. Alternatively, you can [setup a VPN using OpenVPN](../../Network/how-to-configure-client-vpn.md) or similar technology.

2. [Allow incoming traffic](../../Network/how-to-add-public-ip-to-virtual-machine.md) for desired ports by clicking on the Servers Public IP through Control Portal.

1. Add a Public IP to your VM and open Firewall Ports for TCP protocol
1. Browse to the new VM and click on the Add Public IP button
2. When the firewall rule dialog openDs, Add two (2x) single-port boxes: configure one for TCP on port TB 
3. Click the "Add Public IP address button".  When the Add Public IP task completes you should be able to connect to your new Commvault file server from your Commvault client via the public IP. 

### Commvault Blueprints
* Install Commvault Storage on Windows - Deploys Commvault Storage on Windows 2012 server
* Install Commvault AIO - Deploys Commvault Backup and Recovery All In One on Windows

### Steps to deploy Commvault Blueprints
1. Locate the Commvault Blueprints

  1. Starting from the CenturyLink Control Panel, navigate to the Blueprints Library.
  2. Search for “Commvault” in the keyword search on the right side of the page.
  3. Locate the "Commvault" Blueprint for the platform you want to deploy on

  ![Commvault Image](../../images/ecosystem-Commvault-1.png)

2. Choose and Deploy the Blueprint. Click on the “Commvault” Blueprint you want to deploy and then click "Deploy Blueprint" button.

3. Configure the Blueprint. Complete the information below:
  1. Server Administrator Password
  2. Server Group
  3. Network VLAN
  4. Primary DNS - you can use the default of enter 8.8.8.8
  5. Secondary DNS - you can use the default of enter 8.8.8.8
  6. Server Type - Hyperscale `IMPORTANT - Must choose Hyperscale`
  7. Service Level - Premium
  8. Customize the server name, the default is Commvault

    ![Commvault Image](../../images/ecosystem-Commvault-2.png)

4. Review and Confirm the Blueprint.
  1. Click “next: step 2”
  2. Verify your configuration details.

5. Deploy the Blueprint.
  1. Once verified, click on the ‘deploy blueprint’ button. You will see the deployment details along with an email stating the Blueprint is queued for execution.
  2. This will kick off the blueprint deploy process and load a page to allow you to track the progress of the deployment.

6. Monitor the Activity Queue.
  * Monitor the Deployment Queue to view the progress of the blueprint.
  * You can access the queue at any time by clicking the Queue link under the Blueprints menu on the main navigation drop-down.
  * Once the blueprint completes successfully, you will receive an email stating that the blueprint build is complete. Please do not use the application until you have received this email notification.

### Access Commvault File Server
After your Blueprint deploys successfully, please follow these instructions to access your Commvault Server solution:
  1. Check email to obtain Commvault Server information and click on the link to load the server in Control Portal
  2. Connect to the Commvault Server by using Remote Desktop and logging in as Administrator
  3. Find and run “Simpana Administrative Console” from search in windows 2012
  4. Login to the Commserve GUI with the usernamein `admin` and password `admin`
  5. Configure your Commvault solution apprpriately.  See the Post-Requisite section for more details.

### Pricing
The costs associated with this Blueprint deployment are for the CenturyLink Cloud infrastructure only.  There are no Commvault license costs or additional fees bundled in.
Licensing and Pricing for Simpana need to be aligned with software contract.  Please contact CommVault Sales for information: [Contact Commvault sales](http://www.commvault.com/contact-us)

### Frequently Asked Questions 

#### Where do I obtain my Commvault Licenses?
This is a Bring You Own License model (BYOL). [Contact Commvault sales](http://www.commvault.com/contact-us) for license and pricing information. You may obtain a 30 day trail license when you run the blueprint.

#### Who should I contact for support? 
* For issues related to deploying the Commvault solution on CenturyLink Cloud via the Blueprint, Accessing or using the deployed software, [please contact Commvault support](mailto:support@commvault.com) or by calling (877) 780-3077
* For issues related to cloud infrastructure (VM’s, network, etc), or is you experience a problem deploying the Blueprint, please open a CenturyLink Cloud Support ticket by emailing [noc@ctl.io](mailto:noc@ctl.io) or [through the support website](https://t3n.zendesk.com/tickets/new) 
