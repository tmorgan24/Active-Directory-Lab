<h1>Active Directory Home Lab</h1>

 <h2>Description</h2>
In this lab we're going to walk through how to create an Active Directory home lab Enviornmet using Oracle Virtual Box. Configuring and running this lab will definitely help develop your understanding of how active directory and windows networking works, so I'd highhly recommend running through it a couple of times, ask questions where stuff is unclear, and eventually try to build it on your without watching. Also if you scroll down there is a program walk through on how to setup Group Policy Mangement through Active Drirectory. Please let me know if you have any questions!
<br/>


<h2>Languages and Utilities Used</h2>

- <b>Oracle Virtual Box</b> 
- <b>Group Policy Management</b>

<h2>Environments Used </h2>

- <b>Windows 11</b> (21H2)
- <b>Server 2019</b>

<h2>Program walk-through: Setting Up Active Directory

Step 1: Download VirtualBox 

<img width="3903" height="2122" alt="ct4b6lB - Imgur" src="https://github.com/user-attachments/assets/3660ae75-f384-4f65-b118-3618b86bc013" />

Step 2: Download Windows 11 Disk Image (ISO) for x64 devices

<img width="3915" height="2496" alt="aoG2G7R - Imgur" src="https://github.com/user-attachments/assets/343effb4-24e9-4c10-be41-0fc1ad7d0efd" />

Step 3: Download Windows Server 2019 ISO for x64 devices

<img width="3931" height="2260" alt="dwrIXVy - Imgur" src="https://github.com/user-attachments/assets/5b0ef74c-6d1b-47b4-917b-80fe062e4506" />

Step 4: Go to Virtual Box. Click on New. Rename the new VM in this example to DC (Domain Controller) and change the OS Verison to Other Windows (64 bit) and then click on Finish.







<h2>Program walk-through: Group Policy Management Setting Up Password Policy</h2>


Step 1: Go to the start icon and click on it  <br/>
 
 <img width="240" height="320" alt="DqjSHYI - Imgur" src="https://github.com/user-attachments/assets/f8db62f2-28b8-45fc-9e4f-a6144c8dbfa5" />

Step 2: Go to Windows Administrative Tools and click on it  <br/>
<img  />
<br /><img width="240" height="320" alt="IXHHybd - Imgur" src="https://github.com/user-attachments/assets/436d0e88-2869-4258-af34-76fd4a239add" />

Step 3: Go down to Group Policy Management and click on it  <br/>

<img width="240" height="320" alt="fip2HBE - Imgur" src="https://github.com/user-attachments/assets/444cb929-ed70-4239-aa25-1b2f298b81e1" />

Step 4: Click on Forest and then click on domanins and the name of your domain should be under domains  <br/>

 <img width="240" height="320" alt="GZYtLqC - Imgur" src="https://github.com/user-attachments/assets/32b97006-9644-493f-902c-0d4d200eb100" />
 
Step 5: We are going to setup a Password Policy to enforce strong password and enhance security. <br/> 
Right click on your domain and click on Create a GPO in the this domain and link it here.  <br/>

  <img width="240" height="320" alt="UMhYSLS - Imgur" src="https://github.com/user-attachments/assets/b4cac52a-e1a6-427a-b6df-97dc3f7a06ca" />
 
Step 6: Name the New GPO Password Policy and then click on OK <br/>

<img width="240" height="320" alt="TzBycUc - Imgur" src="https://github.com/user-attachments/assets/542d5ee7-3094-439c-a649-bc07049dc307" />
 
Step 7: Password Policy is now under your domain. Now right click on Password Policy and now click on Edit <br />

<img width="240" height="320" alt="TfEuPcr - Imgur" src="https://github.com/user-attachments/assets/74d783fa-0b33-4d12-a63b-5f5495c523c0" />

Step 8: Now you see the Group Policy Management Editor. Now you have to figure out wheter to setup the policy under the computer configuration or user configuration. It should be under computer configuration because it's the computer that is asking for the password when logging in. <br/>
Now as IT proffessional you have to figure out if it's under policies or preferences? It would be under policies it should never be changed by the user 
and it should be enforeced by administrators. <br/>

<img width="240" height="320" alt="EL4B5jX - Imgur" src="https://github.com/user-attachments/assets/923d8b75-975d-4922-ad30-6235c7565fcd" />
 
Step 9: Click on Policies. Then click on Windows Settings (Because it is going to used under windows) <br/>

<img width="240" height="320" alt="LtMUfK7 - Imgur" src="https://github.com/user-attachments/assets/79826d63-ab56-44e0-b1fb-50ec7cc2f4b2" />
<img width="240" height="320" alt="yXDc7rl - Imgur" src="https://github.com/user-attachments/assets/368681f7-fd9c-4c46-ba29-6dc66ef12ca4" />
 
 Step 10: Click on Security Settings (because password is a security setting). Then click on Account Policy <br/>

<img width="240" height="320" alt="vwVKPtA - Imgur" src="https://github.com/user-attachments/assets/f4baeba5-a94f-4fa3-bcee-8a0d4b484e4d" />
<img width="240" height="320" alt="WgrGi0u - Imgur" src="https://github.com/user-attachments/assets/7610a671-8ec2-4afb-bd04-1f5c1461f6a1" />


Step 11: Click on Password Policy. On the right side you can see the different password policy settings.

<img width="240" height="320" alt="78PPYms - Imgur" src="https://github.com/user-attachments/assets/95e75eea-f292-4ae7-b577-5a1469a38fe8" />

Step 12: We are going to change the minimum password length. Now double click on minimum password length. Then click on define this policy setting.
Then under log adult events when new passwords are shorter than: and type in 12 in the box. Then click on apply and then ok. Then the setting should
be change to 12 characters. <br/>

<img width="240" height="320" alt="v99m2pa - Imgur" src="https://github.com/user-attachments/assets/f40eaafd-eb82-4ac8-904e-2ddf0340200e" />
<img width="240" height="320" alt="rQjitXI - Imgur" src="https://github.com/user-attachments/assets/9cac3a80-0800-44be-8382-d9588a8fd28a" />
<img width="240" height="320" alt="t1Jlikr - Imgur" src="https://github.com/user-attachments/assets/57ca24f0-f7da-494b-aee2-1e69ad743c0a" />
<img width="240" height="320" alt="CXtpbqC - Imgur" src="https://github.com/user-attachments/assets/d744f5f1-023a-44d8-a5c4-7aa5457fd352" />


Step 13: Now double click on password must meet complexity requirements. Then click on define this policy setting. Then click on enabled so that the 
password meets the complexity requirements that windows has setup for every computer that has this group policy. Click on Apply and then OK. And 
that policy is setup. <br/>

<img width="240" height="320" alt="fJt2Rl5 - Imgur" src="https://github.com/user-attachments/assets/9720f4cb-0738-4266-95db-fd67f5f5afc3" />
<img width="240" height="320" alt="pONwPcV - Imgur" src="https://github.com/user-attachments/assets/2ee05569-6e59-4704-abde-484e41d4d828" />
<img width="240" height="320" alt="mbiTSGi - Imgur" src="https://github.com/user-attachments/assets/1ce57934-f003-48d4-a7aa-aa524544c44d" />
<img width="240" height="320" alt="gMAtoAN - Imgur" src="https://github.com/user-attachments/assets/84559e1a-a135-45c8-b0d3-412f972a7124" />

Step 14: Next you can change the maximum password age by right clicking on it. Click on this policy setting. Depending on your company and how many 
many days they want to change the password, but for this example we are going to say every quarter which is 90 days. So type in 90. Then click
apply. The computer is going to suggest 30 days just go ahead and hit ok. Then hit ok again. And now you can see that policy has been changed. <br/>

<img width="240" height="320" alt="iL9G6kj - Imgur" src="https://github.com/user-attachments/assets/7aad3a33-e48c-40c1-8f69-23b19e20b568" />
<img width="240" height="320" alt="qYwiQRU - Imgur" src="https://github.com/user-attachments/assets/9c6ae793-8362-40cc-bcf6-cf21da1d9fc8" />
<img width="240" height="320" alt="S15asw1 - Imgur" src="https://github.com/user-attachments/assets/63187b04-36c1-450d-9f10-164f5225799b" />
<img width="240" height="320" alt="UEhoa7l - Imgur" src="https://github.com/user-attachments/assets/603dfdf7-b1aa-4b3c-aca8-8c8c27477878" />
<img width="240" height="320" alt="4gMg3IA - Imgur" src="https://github.com/user-attachments/assets/9e427276-803e-4f9f-884b-ea3037f6a61e" />
<img width="240" height="320" alt="gaDD4Ei - Imgur" src="https://github.com/user-attachments/assets/31831212-5ec7-4d9e-a1f1-5ae447906315" />

And that's how you can setup a Password Policy through Group Policy Management on Active Directory. 

