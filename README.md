# Azure Virtual Machine Setup

<h2>Table of Contents</h2>

1. Create a Resource Group
2. <a href="https://github.com/ian-bates-it/Azure-Virtual-Machine-Setup?tab=readme-ov-file#create-a-windows-10-pro-virtual-machine-version-22h2">Create a Windows 10 Pro Virtual Machine in Azure</a>
3. <a href="">Create a Windows Server in Azure</a>





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

<img src="https://github.com/user-attachments/assets/9e9149e8-f618-4976-86a8-af3227bd4d47" height="80%" width="80%" />

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


---
<br />
<br />

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


<h3>Instance Details</h3>

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






