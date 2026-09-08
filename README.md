<p align="center">

<h1>Configuring Active Directory</h1>
The objective of this project was to utilize a domain controller and client virtual machines created here (https://github.com/JMW814/creating-azure-vms) to simulate a domain/Active Directory environment for testing, building an intuition for it, and using it for subsequent labs/projects. 
<h2>Environments and Technologies Used</h2>

- Microsoft Azure
- Virtual Machine 1 (Client-1)
- Virtual Machine 2 (Domain Controller/DNS Server)
- Remote Desktop
- DNS Manager
- Active Directory

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)


<h2>Deployment and Configuration Steps</h2>

To create the test environment for this demonstration, I used 2 virtual machines created here (https://github.com/JMW814/creating-azure-vms)  
 
 Step 1
 
In DC-1, I opened Server Manager to install Active Directory <p>
<img width="930" height="573" alt="image" src="https://github.com/user-attachments/assets/3bf632e7-c1dc-4208-b5ba-4e406425933f" />

</p>
<p>
Step 2
 
 Next, now that I have downloaded Active Directory, I needed to promote DC-1 to a domain controller for it to work. 
 
 I added a new forest and named the domain "mydomain.com" 
</p>
<br />

<p>
<img width="519" height="380" alt="image" src="https://github.com/user-attachments/assets/588272d2-3bd9-4a35-8028-d02f3a18db3d" />



</p>
<p>
 
Step-3
 
Now that the domain is active, I logged back in to Client-1 and added it to the domain
<p>
<img width="560" height="658" alt="image" src="https://github.com/user-attachments/assets/1ee3a855-f877-46eb-a2ff-714966896a9a" />


</p>
<p>
Step-4
 
Now that Active Directory is installed and the client machine is connected to the domain, I want to practice using Active Directory as an administrator by creating my own workplace environment filled with users, groups, and units.

I started by creating 4 organizational units for accounting, clients, admins, and employees
<p>
<img width="1269" height="768" alt="image" src="https://github.com/user-attachments/assets/0398331c-f6ec-4334-943b-a53ff2f651e7" />


</p>
<p>

</p>
<br />
Next, I want to add a bunch of employee accounts to the domain so I can experiment with them. I used this script in PowerShell ISE (https://github.com/joshmadakor1/AD_PS/blob/master/Generate-Names-Create-Users.ps1) to simultaneously create thousands of user accounts for me to use, so I didn't have to create them by hand.


<p>
<img width="1791" height="949" alt="image" src="https://github.com/user-attachments/assets/26420514-6b9d-4e8d-b79a-d5584da7de30" />


</p>
<p>
Step 5
Finally I practiced moving users around different security groups, by promoting one of the created users to a domain admin. 

<p>
<img width="1046" height="747" alt="image" src="https://github.com/user-attachments/assets/a9a4d3d3-e1ff-4059-9086-deef8847c313" />


</p>
<p>
</p>
<br />
<h2>Conclusion</h2>
I was able to build my intuition for Active Directory by creating a domain controller, connecting a client machine to the domain, and creating a testing foundation in Active Directory.
