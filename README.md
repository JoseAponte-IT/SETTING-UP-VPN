![image](https://github.com/user-attachments/assets/9433fa98-17a9-4a0d-89b7-9d19da194bc3)

# Configuring a VPN on an Azure Virtual Machine
This project demonstrates how to configure a VPN within an Azure Virtual Machine using ProtonVPN, showcasing a foundational understanding of VPN concepts, configuration, and practical applications. Through this hands-on lab, we verify the VPN connection by observing changes in the public IP address and exploring geo-locked content.🫡

<h1>osTicket: Post-Installation Configuration</h1>


<h2>Tools & Technology Used</h2>

- Microsoft Azure: Virtual Machine hosting.

- RDP: For remote access to the VM.

- ProtonVPN: VPN configuration and connection.

- WhatsMyIPAddress: Verifying public IP address changes.

<h2>Key Objectives:</h2>

- Set up a VPN on a Windows 10 Azure Virtual Machine.

- Understand the purpose and functionality of a VPN for security, privacy, and accessibility.

- Verify the VPN connection using tools like whatsmyipaddress to observe changes in the public IP address.

- Access geo-restricted content, showcasing real-world VPN use cases.

<h2>Prerequisites</h2>

- An active Microsoft Azure Subscription

- Microsoft RDP: If on MAC go to APP Store and download Microsoft RDP

- ProtonVPN account (or an equivalent VPN service).

# Project Overview
- Go to Azure Portal

![image](https://github.com/user-attachments/assets/6f75e551-4d66-4af6-a20e-8a1f6fa831fe)

- Go to Resource Group

![image](https://github.com/user-attachments/assets/37506426-1785-44af-8dff-d2fbf4735d20)

- Create Resource Group

![image](https://github.com/user-attachments/assets/d1571f43-284a-4721-b0ad-1d170b33273e)

- Name the Resource Group

![image](https://github.com/user-attachments/assets/c45b31c1-83c8-4e6e-8e25-20b0be0eb104)

- Review and Create Resource Group

![image](https://github.com/user-attachments/assets/b98e48a6-a504-44df-899a-2b91a9354f7e)

- Create Resource Group

![image](https://github.com/user-attachments/assets/cfa87af7-f3c9-44aa-8912-4d34c05ed2b8)

- Resource Group Succesfully created

![image](https://github.com/user-attachments/assets/c2859c23-b3cb-4c60-89ca-c436937415ed)

<H2>Step 2: Creating Resource (Virtual Machine)</H2>

- Return to the Azure Portal and find the "Virtual Machines" option (You can search it in the searchbar if you cant find the option in the dashboard) 

![image](https://github.com/user-attachments/assets/37ac9f7a-e86c-44b7-aa37-d125469a692f)

- Create a virtual machine resource 

![image](https://github.com/user-attachments/assets/64829dcf-3278-4353-a19d-dc6f9425a77f)

- Assign the VM to the Resource Group that was created

![image](https://github.com/user-attachments/assets/d101a9e4-3db9-4de2-b485-556884d23b03)

- Fill out these details:<br> 
-Virtual Machine Name<br>
-Region [!!IMPORTANT!! Make sure that the region used to create the resource group is the same as the region as the VM you are creating, might run into issues otherwise] <br>
-Image [we are going to make a Windows 10 VM so make sure to select the Windows 10 pro option for image]<br>

![image](https://github.com/user-attachments/assets/6d08279c-cba8-4fa2-94d2-1f180a82f7e9)

- For optimal performance I will use 2cpus as the standard size<br>

![image](https://github.com/user-attachments/assets/08cfa758-8454-4343-9665-f5081ebfdd80)

- Create Username and password 

![image](https://github.com/user-attachments/assets/028d853e-63a4-4d23-938e-b3c39daa1d01)

Confirm Licensing 

![image](https://github.com/user-attachments/assets/d25e7c66-a950-461c-a7fb-6e1109460123)

- Review and Create 

![image](https://github.com/user-attachments/assets/bdce6266-ec36-43a7-9aaa-9ec34b2c6a10)

![image](https://github.com/user-attachments/assets/dd270697-8d60-4b08-944e-e45ddae3e3ca)

- Virtual Machine (Windows 10 Pro) Successfully Created.<br>
Osbervations: When creating our VMs, a Virtual Network,Virtual NIC, IP Address abd Network Security Group will be automatically created.<br>[Essentially all the necessary network infrastructure so that the VM can have its own network to transfer data locally and to the internet]  

 ![image](https://github.com/user-attachments/assets/8b856f5e-c4e7-4184-9aa2-6d57d43d3930)

<h2>Step 3: Creating our Second Resource (Virtual Machine)</h2>

<h2>Step 4: Use RDP to login into the VM </h2>

- Return to the Virtual Machine Dashboard in the Azure portal

![image](https://github.com/user-attachments/assets/a2e686dc-d035-432b-a079-18927560bc76)

- Jot down the Public IP adresses of the VM's 

![image](https://github.com/user-attachments/assets/1a8e4a73-f175-42fb-bb68-6ba3ab1b18ba)

- If on Windows press Windows key -> Open RDP If on MAC download RDP program in APP store and put in the IP adress of the Windows VM 

![image](https://github.com/user-attachments/assets/5f159faa-a725-4e26-b101-de3f7121278e)

- Enter the Log in credentials and log in to the machine 

![image](https://github.com/user-attachments/assets/ea9d83e9-20e4-4f72-860a-85defe141e06)



====
<h2>Step 5: Observe public IP address and notice how it will change later  </h2>

- Navigate to www.whatismyipaddress.com inside your VM.
- Observe your IP address and the content available without using a VPN. 

- This will help you understand how a VPN impacts the content you can access by virtually placing you in another region. This process, known as IP spoofing, works by routing your data through a secure virtual tunnel to a VPN server before it reaches the web. The VPN acts as an intermediary, masking your original IP address and making it appear as though your traffic originates from the server's location.

![image](https://github.com/user-attachments/assets/92f0de20-5403-4d3a-8e61-907e371b7479)

![image](https://github.com/user-attachments/assets/6d92956e-4fbe-40f1-aad2-d78440f31726)

<h2>Step 6: Install and sign up to Proton VPN (It's Free ) </h2>

- Go to protonvpn.com 

- Install ProtonVPN according to your Operating System. 

![image](https://github.com/user-attachments/assets/f73a3d57-98ee-4ce0-9fa3-fd140ec6ec04)

![image](https://github.com/user-attachments/assets/a6afa158-1c7c-4f45-9c0a-c8eea818c708)

![image](https://github.com/user-attachments/assets/22c7f35c-e76c-4939-a9c6-361e6fa1d56f)

![image](https://github.com/user-attachments/assets/75c12eba-9913-40df-ab2b-b1847517d214)

<h2>Step 7: Login and Select your VPN Server </h2>

- Log in to ProtonVPN.

![Annotation 2024-07-06 230943](https://github.com/erik-salgado/VPN-Setup/assets/173113320/c6077764-a742-4d57-975b-2f32264ab808)

- Select VPN Server.

![image](https://github.com/user-attachments/assets/1104acab-f89d-4892-b5aa-75e56329d48c)


![image](https://github.com/user-attachments/assets/a93cce2e-7e70-4eaf-8688-ddbec708abad)

<h2>Step 8: Confirm and Observe IP adress changes and how it affects the content you see </h2>

- Go to www.whatismyipaddress.com using your new vpn server.

![image](https://github.com/user-attachments/assets/205040fc-c891-4b02-9788-0c9041d6e06d)

- The IP Address will now be different as a result of setting up our VPN. 
- The Netherlands was selected. Since my location has been changed, content that may have been geo locked to the Netherlands will now be available to me.

![image](https://github.com/user-attachments/assets/20df319f-ac76-4557-ac2b-91bb24ec1d1e)

![image](https://github.com/user-attachments/assets/f64579e3-8f9a-452b-8265-0a2826624a8f)


# 🎉Congratulations

<h2>We Have Successfully:</h2>

- Configured a VPN within an Azure Virtual Machine.

- Verified the VPN connection by observing the public IP address change via WhatsMyIPAddress.

- Demonstrated how a VPN allows access to geo-restricted content.

- Showcased practical knowledge of VPN setup, functionality, and real-world use cases.

# That Concludes this lab<img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="30px"/>

