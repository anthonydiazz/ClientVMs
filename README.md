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
