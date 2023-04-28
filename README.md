<h1>LetsDefend - SOC146 - Phishing Mail Detected - Excel 4.0 Macros</h1>


<h2>Alert</h2>
Received an alert that a phishing email has been detected.
<br />
![image](https://user-images.githubusercontent.com/131769679/235142645-20231d35-82e8-49c1-8953-df7b1614a8fe.png)


<h2>Information Gathered</h2>

- <b>SMTP Address: 24.213.228.54</b> 
- <b>Source Address: trenton@tritowncomputers.com</b>
- <b>Dest. Address: lars@letsdefend.io</b>
- <b>E-mail Subject: RE: Meeting Notes</b>
- <b>Device Action: Allowed</b>

<h2>Are there attachments or URLs in the email? </h2>

- <b>Yes, a zip file named "11f44531fb088d31307d87b01e8eabff.zip" is attached. No URLs.</b>

<h2>Analyze URL/Attachment</h2>

- <b>By uploading the file to hybrid-analysis we can see that the three files inside are malicious. Looking at the "research-1646684671.xls" file we can see that the file tries to contact 5 domains and 3 hosts.</b>

![image](https://user-images.githubusercontent.com/131769679/235143528-a2090f1f-e501-4873-80a2-430f4f20237e.png)
![image](https://user-images.githubusercontent.com/131769679/235143564-2350a084-27da-4bf0-8b58-db92547011e3.png)
![image](https://user-images.githubusercontent.com/131769679/235143591-e08169cf-5d72-44de-b72c-a4448ff30e71.png)

<h2>Check If Mail Delivered to User</h2>

- <b>The alert stated that the Device Action was Allowed, confirming that the email was delivered. The email was removed.</b>

<h2>Check If Someone Opened the Malicious File/URL</h2>

- <b>After reviewing the logs I can confirm that the local IP connected successfully to the C2 server we found earlier. So the host did execute the file. The host was contained.</b>

![image](https://user-images.githubusercontent.com/131769679/235143867-7479a35f-5bc6-49e9-bd9e-28c02b6c6f83.png)
![image](https://user-images.githubusercontent.com/131769679/235143875-6b454fde-2d2a-46bc-8815-339a2b9cedf5.png)
![image](https://user-images.githubusercontent.com/131769679/235143891-83743391-2ec4-432f-a191-1a50588e02d1.png)


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
