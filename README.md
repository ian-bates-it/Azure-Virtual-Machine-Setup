<p align="center">
<img src="https://github.com/user-attachments/assets/6b153b0d-e780-42c1-aaa7-e978aa687226" height="20%" width="20%"/>
</p>

<h1>Chapter 1: Azure Virtual Machine Setup</h1>
This tutorial outlines the implementation of Azure Virtual Machines. We will first create a resource group named `Network-Testing-RG` and then create a Windows 10 Virtual Machine and a Windows 2022 Server VM as part of the `Network-Testing-RG` resource group.<br />

---

<h2>High-Level Deployment and Configuration Steps</h2>

<!--
1. Step 1: <a href="https://github.com/ian-bates-it/Azure-Virtual-Machine-Setup/edit/main/README.md#create-a-resource-group">Create a Resource Group</a>
2. Step 2: <a href="https://github.com/ian-bates-it/Azure-Virtual-Machine-Setup?tab=readme-ov-file#create-a-windows-10-pro-virtual-machine-version-22h2">Create a Windows 10 Pro Virtual Machine in Azure</a>
3. Step 3: <a href="https://github.com/ian-bates-it/Azure-Virtual-Machine-Setup/blob/main/README.md#create-a-windows-2022-server-virtual-machine-datacenter-azure-edition---x64-gen2">Create a Windows 2022 Server in Azure</a>
-->

1. Part 1: [Create a Resource Group](https://github.com/ian-bates-it/Azure-Virtual-Machine-Setup/edit/main/README.md#create-a-resource-group)
2. Part 2: [Create a Windows 10 Pro Virtual Machine in Azure](https://github.com/ian-bates-it/Azure-Virtual-Machine-Setup?tab=readme-ov-file#create-a-windows-10-pro-virtual-machine-version-22h2)
3. Part 3: [Create a Windows 2022 Server in Azure](https://github.com/ian-bates-it/Azure-Virtual-Machine-Setup/blob/main/README.md#create-a-windows-2022-server-virtual-machine-datacenter-azure-edition---x64-gen2)

---

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<br />
<br />

---

<h1>Part 1:</h1>

<h2>Create a Resource Group</h2>

 - Log into Azure (<a href="https://portal.azure.com/" target="_blank">portal.azure.com</a>)
<br />
<p>You can search for `Resource Groups` and select the icon as shown below:</p>
<br />
<img src="https://github.com/user-attachments/assets/12cf0b4e-201d-4e73-8095-af7138aa69ac" height="80%" width="80%" />

---

Select the `+ Create` button 
<br />
<br />
<img src="https://github.com/user-attachments/assets/21d24f65-5a98-4667-b46c-61f53a9f29db" height="80%" width="80%" />


---
<br />
<h4>Resource Group Basics</h4>

1. Select the appropriate Subscription. Using the free account, I selected my `Azure subscription 1`.
2. Add a name for the resource group. I named my resource group `RG-Network-Testing`.
3. Select a data center region, preferably a location close to you. I selected `(US) Central US`
4. Click the `Review + Create` button

<img src="https://github.com/user-attachments/assets/9e9149e8-f618-4976-86a8-af3227bd4d47" height="60%" width="60%" />

<br />

---

<h4>Confirm and Select Create</h4>
- Select the `Create` button
<br />
<br />
<img src="https://github.com/user-attachments/assets/892b6ccb-680e-4470-a63a-a7bbc42de33f" height="50%" width="50%" />

---
<br />

<h4>Now we have the Resource Group we can use to set up our Windows Server and Windows 10 Pro virtual machines. </h4>


<img src="https://github.com/user-attachments/assets/4800896e-2792-4802-88fd-0dcadd207ae3" height="80%" width="80%" />


<br />
<br />

---

<h1>Part 2:</h1>

<h2>Create a Windows 10 Pro Virtual Machine (version 22H2)</h2>


<!--
<img src="" height="80%" width="80%" />

-->

<h4>Search for Virtual Machines. Select the VM Icon</h4>

- Search for Virtual Machines
- Select the Virtual Machine icon as shown below:

<img src="https://github.com/user-attachments/assets/24fc00d8-8c41-4881-827d-eeb78277a9cd" height="80%" width="80%" />

<br />


---

<h3>Select `Create` => Azure Virtual Machine </h3>

 - Select the Create button
 - Select the `Azure Virtual Machine` option as shown below

 <img src="https://github.com/user-attachments/assets/985a2950-d5a8-4186-be6e-5575c38141aa" height="80%" width="80%" />


---

<h3>Project Details Section</h3>

- <b>Subscription</b>
  - Select the appropriate subscription.
  - Here I selected `Azure subscription 1`.
- <b>Resource Group</b>
  - The virtual machine must belong to a resource group.
  - Select the resource group created as shown above from the drop-down menu.
   -  My resource group was named `Network-Testing-RG`.

     <br />  
   --

<img src="https://github.com/user-attachments/assets/64e03529-3a68-43fe-9618-3dd55e752a65" height="80%" width="80%" />

<br />

---


<h3>Instance Details Section</h3>

1. Add a name for the virtual machine
   - I called mine `Windows-10-Pro-VM`
2. Select the same region as your resource group
   - In my case, I selected `(US) East US` from the drop down menu. 

<img src="https://github.com/user-attachments/assets/9d954e1f-5789-4aef-94e4-135a87dce31a" height="80%" width="80%" />




3. <b> Virtual Machine Image</b>
   - From the drop down menu, select the `Windows 10 Pro, version 22H2 - x64 Gen2` or similar Windows 10 Pro option available to you.
   - Accept the default optoins for the rest of the fields in this `Instane Details` section.

<img src="https://github.com/user-attachments/assets/7cf64630-d66b-432d-884a-f694539776af" height="80%" width="80%" />


<br />
<br />

4. <b>Virtual Machine Size</b>
 - Select the desired size of the virtual machine.
 - It is recommended to pick something with at least 2 vcpus
 - I selected the `Standard_D2s_v3 - 2vcpus, 8 GiB memory` 

<img src="https://github.com/user-attachments/assets/685e242b-ecb0-499f-8448-92342c822b97" height="80%" width="80%" />



---

<h3>Administrator Account</h3>

- Create the default administrator Username and Password for the virtual machine.
- I chose `helpdesk` as my username

<img src="https://github.com/user-attachments/assets/5011d726-a8e0-4a9a-a165-2b0006803397" height="80%" width="80%" />


---

<h3>Select the `Disks >` Button</h3>

- Accept the default options for the remaining fields in the `Basic` tab section.
- Click the `Disks >` button at the very bottom to continue as shown below.

<img src="https://github.com/user-attachments/assets/3df57159-e4b9-4b23-b2e6-ad5b75d6062c" height="80%" width="80%" />


---

<h3>Disks Tab</h3>

- Accept all the default options for the Disks Tab.
- Click the `Next: Networking >` button at the very bottom to continue as shown below.

<img src="https://github.com/user-attachments/assets/5a3b9199-322a-4742-a7d6-b955f7cc9bb6" height="80%" width="80%" />

---


<h3>Networking Tab</h3>

<!--
- In the networking tab, select the `Create new` link in the **Virtual network** field as shown below.

<img src="https://github.com/user-attachments/assets/9701fb64-1ab7-4d94-89dd-be8a977c03bf" height="80%" width="80%" />

<br />
<br />
-->

1. In the **networking tab**, select the `Create new` link in the **Virtual network** field as shown below.
2. Create a name for the Virtual Network. I called mine `helpdesk-vm`
3. Click the Okay button as shown below.

<img src="https://github.com/user-attachments/assets/8327159b-1cf9-4d88-ba99-2ccd14f1a2b8" height="100%" width="120%" />


- Accept the defaults for everything else in the Networking Tab
- Click the `Review + Create` blue button at the bottom of the page as shown below to continue.

<img src="https://github.com/user-attachments/assets/6c50286f-8eee-416e-945a-2103f6c91c69" height="80%" width="80%" />


---

<h3>Review and Create Windows 10 Pro Virtual Machine</h3>

- Azure will validate your settings and confirm that your settings passed the validation test
- Click the blue `Create` button at the bottom of the screen to create your Windows 10 Pro virtual machine as shown below

<img src="https://github.com/user-attachments/assets/3a0bbddd-2a13-429b-a4e8-bdc241e445bf" height="70%" width="80%" />


---

- After Azure completes building your virtual machine you will get a confirmation message like the one shown below.

<img src="https://github.com/user-attachments/assets/7bf9e51e-f265-4e49-964f-96a19e6638c4" height="30%" width="30%" />



<br />
<br />

---

<h1>Part 3:</h1>

<h2>Create a Windows 2022 Server Virtual Machine (Datacenter: Azure Edition - x64 Gen2)</h2>


---
<h4>Go to Virtual Machines</h4>

- Use the search bar to find Virtual Machines and select the Virtual Machine icon as shown below.


<img src="https://github.com/user-attachments/assets/32545e20-9c89-444c-bfaf-299686dab989" height="40%" width="40%" />


---


<h3>Create Azure Virtual Machine</h3>

- Select the `+ Create` button
- Select the `Azure virtual machine` option from the drop-down menu

<img src="https://github.com/user-attachments/assets/8365cda4-4592-4086-8101-12cc2ef0ee00" height="80%" width="80%" />


---

<h3>Project Details Section</h3>

1. Select your subscription. Here I selected my `Azure subscription 1`
2. Select the same resource group we selected above in the Windows 10 Pro VM.
   - In this example, that resource group was `Network-Testing-RG` as shown below.

<img src="https://github.com/user-attachments/assets/e159ecd7-8fb0-468a-9735-9a6555d8e3b2" height="80%" width="80%" />
  

---
<br />
<h3>Instance Details Section</h3>

1. Name the Windows Server virtual machine. Here I named mine `Windows-2022-Server-VM`.
2. Select the same region you selected above for the Resource Group and the Windows 10 Pro VM.
   - In this example, my region for everything was `(US) East US` as shown below.
  

<img src="https://github.com/user-attachments/assets/2375764c-881f-4d4d-b657-ef0e9af53344" height="80%" width="80%" />


---
<br />

<h3>Virtual Machine Image</h3>

3. From the drop-down menu, select the `Windows Server 2022 Datacenter: Azure Edition - x64 Gen2` image from the drop down menu as shown below.

<img src="https://github.com/user-attachments/assets/e8e13600-6498-43e6-a6d9-6ca08e69520e" height="80%" width="80%" />


---
<br />

<h3>Virtual Machine Size</h3>

4. Select the size of the Windows Server virtual machine. It is recommended that you select something with 2 vcpus.
   - Here I selected the option `Standard_D2s_v3 - 2 vcpus, 8 GiB memory` as shown below.

  <img src="https://github.com/user-attachments/assets/d47d5d96-78c3-4a76-9c20-75798a88ca59" height="80%" width="80%" />


---
<br />


<h3>Virtual Machine Size</h3>

1. Create a username and password for the Windows Server administrator account.
   - Here I created a username of `Admin-DC` as shown below. 
2. Select the `Next : Disks >` button at the bottom of the screen to continue as shown below

  <img src="https://github.com/user-attachments/assets/92cca3de-c424-4aa1-b788-071549e94dce" height="80%" width="80%" />


---
<br />

<h3>Disks Tab</h3>

- Accept the default options in the Disks Tab.
- Click the `Next : Networking >` tab at the bottom of the screen as shown below.


  <img src="https://github.com/user-attachments/assets/046524db-8159-4552-87bd-c66b0788d6fe" height="80%" width="80%" />


---
<br />

<h3>Networking Tab</h3>

1. Make sure the Windows Server Virtual Network is set to the virtual network we created above in the Windows 10 Pro VM. Here, my virtual network was `helpdesk-vm`.
2. Click the blue `Review + Create` button at the bottom of the screen to complete the installation as shown below.

  <img src="https://github.com/user-attachments/assets/2d65cb81-e41f-47bf-9566-cf4349a53bf0" height="80%" width="80%" />


---
<br />


<h3>Review and Create Windows 2022 Server Virtual Machine</h3>

- Azure will validate your settings and confirm that your settings passed the validation test
- Click the blue `Create` button at the bottom of the screen to create your Windows 10 Pro virtual machine as shown below

<img src="https://github.com/user-attachments/assets/2d4dc629-bcfd-4ea1-ac6a-a4a8c5d5d0bd" height="70%" width="80%" />


---
<br />

- Allow a few minutes for Azure to complete building your Windows Server virtual machine. Then you will get confirmation that the Windows Server is complete. It will look something like what is shown below.

<img src="https://github.com/user-attachments/assets/9ed2e1f4-ca0a-429d-9b93-4c0f6394b5b8" height="70%" width="80%" />


---




