<img width="1752" height="897" alt="Secure Azure Service Bus Network Architecture" src="https://github.com/user-attachments/assets/255ebc12-83ec-4923-82d4-56f7d504889f" />
Step 1 — Create a Resource Group
A Resource Group is where Azure organizes related resources.

    1. Open Azure Portal.
    2. Search for Resource groups.
    3. Click Create.
    4. Choose your subscription.
    5. Enter rg-network-lab.
    6. Select East US.
    7. Click Review + create → Create.
    Verify: Go to Resource groups and confirm rg-network-lab appears.

Step 2 — Create your Virtual Network
    1. Search for Virtual networks.
    2. Click Create.
    3. Select resource group rg-network-lab.
    4. Enter vnet-network-lab.
    5. Choose East US.
    6. Open the IP addresses tab.
    7. Set IPv4 address space to 10.10.0.0/16.
    8. Add these subnets:
    Subnet name	Address range
    snet-app	10.10.1.0/24
    snet-private	10.10.2.0/24
    
    9. Click Review + create → Create.
    Why two subnets?
    The application subnet holds your VM. The private subnet holds the Private Endpoint network interface.
    
    The VM might receive 10.10.1.4, while the endpoint might receive 10.10.2.4. Azure assigns the actual addresses.
    
    Verify: Open vnet-network-lab → Subnets. Both subnets should be visible.
