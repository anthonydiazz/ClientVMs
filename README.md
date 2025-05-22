# Part 2: Client VM Setup, Domain Join & GPO Enforcement

This section covers the deployment and configuration of two Windows 10 client machines that connect to the internal network, join the domain anthonytech.com, and are managed via group policies. You will:

- Set up Windows 10 VMs in VirtualBox
- Join both clients to the domain
- Log in with created domain users (Helpdesk and Bruce Wayne)
- Install RSAT tools on the Helpdesk machine
- Create and apply a GPO that disables Task Manager for User (Bruce Wayne)

## Step 1: Create and Configure Windows 10 VMs

Each Windows 10 VM should be created in VirtualBox and configured as follows:

- Adapter 1: Internal Network (same name as used by the server, e.g., intnet)

![Install Requests](./ad_p2/p1.png)


## Step 2: Domain Join (Desktop1) - Helpdesk User 


1. Go to System Properties > Computer Name

2. Rename the PC to Desktop1

3. Click "Change" and join the domain: anthonytech.com

4. When prompted, enter credentials for a domain admin account

5. Reboot when prompted

![Install Requests](./ad_p2/p4.png)


## Step 3: Log in with Domain User (Helpdesk)

1. After rebooting Desktop1, log in using the domain credentials:

- Username: helpdesk

- Domain: anthonytech.com

![Install Requests](./ad_p2/p5.png)


## Step 4: Confirm IP and DNS Configuration

1. Open Command Prompt and run ipconfig /all

2. Verify:

- IP is from DHCP (192.168.0.x)

- DNS points to server (192.168.0.1)

- Domain suffix is anthonytech.com

![Install Requests](./ad_p2/p6.png)



## Step 5: Install RSAT Tools (Helpdesk User Only)

1. On Desktop1 (logged in as Helpdesk), open "Optional Features"

2. Install the following RSAT tools:

- Active Directory Domain Services

- DNS

- DHCP

- Group Policy Management

- Remote Access

![Install Requests](./ad_p2/p8.png)


3. After installation, verify the tools appear under "Windows Administrative Tools"


![Install Requests](./ad_p2/p9.png)







