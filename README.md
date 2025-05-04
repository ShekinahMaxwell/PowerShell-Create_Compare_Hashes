# PowerShell-Create_Compare_Hashes
<p align="center">
<img src="https://upload.wikimedia.org/wikipedia/commons/2/2f/PowerShell_5.0_icon.png" alt="PowerShell Logo"/> 
</p>

<h1> Create and Compare Hashes Lab Exercise</h1>
This tutorial outlines the use of Hashing to help determine data integrity<br />

<h2>Environments and Technologies Used</h2>

- Windows PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1: Create a new file folder 
- Step 2: Create a text file from within the folder
- Step 3: Enter commandline on PowerShell and type command "Get - FileHash" along with the name of the text file
- Step 4: Notice the output Hash for the file. Run the same command again and notice the hash for the file is still the same.
- Step 5: Change the text file's content
- Step 6: Run the command "Get - FileHash" again
- Step 5: Notice the Hash is now different

<h2>Deployment and Configuration Steps</h2>

<p>
<img width="1328" alt="Screen Shot" src="https://github.com/user-attachments/assets/c9a7a52f-b7e1-4436-95cf-c2e2ce21706b"/>
<img width="1184" alt="Screen Shot 2025-05-04 at 4 24 10 PM" src="https://github.com/user-attachments/assets/c61a1e3e-74f4-443d-aae7-a70a6d91e491" />
</p>
<p>
Create a new file folder and name it "HashExample". Right-click the desktop > New > Folder
</p>
<br />

<p>
 <img width="1338" alt="Screen Shot 2025-05-04 at 4 12 08 PM" src="https://github.com/user-attachments/assets/86c90512-56c6-47db-8c46-b02bb79d14a7" />
 <img width="1284" alt="Screen Shot 2025-05-04 at 4 17 15 PM" src="https://github.com/user-attachments/assets/43ec702e-e4c1-4948-a3bb-90ac8f0a5c07" />
</p>
<p>
Within folder, create a new Text Document. Right-click the "HashExample" folder > New > Text Document > Name the file "Md5sum" for example
</p>
<br />

<p>
<img width="1162" alt="Screen Shot 2025-05-04 at 4 29 09 PM" src="https://github.com/user-attachments/assets/2a69fe11-54cd-48f0-ad32-34c1abedb4df" />
<img width="1210" alt="Screen Shot 2025-05-04 at 4 29 55 PM" src="https://github.com/user-attachments/assets/5bd0ff7e-bc7b-418f-b268-94be12996362" />
<img width="1168" alt="Screen Shot 2025-05-04 at 4 30 40 PM" src="https://github.com/user-attachments/assets/49f11716-89f7-4836-a386-4397f0619a57" />
</p>
<p>
Right click the "Md5sum" Text Document > Open > Type in a message, "Hello" for example > File > Save 
</p>
<br />

<p>
<img width="1329" alt="Screen Shot 2025-05-04 at 4 31 28 PM" src="https://github.com/user-attachments/assets/c036ae00-51e5-4511-85ef-670421ff4cda" />
<img width="1137" alt="Screen Shot 2025-05-04 at 4 43 41 PM" src="https://github.com/user-attachments/assets/f80b077f-af8c-4c38-8b05-e893475108ad" />
<img width="1141" alt="Screen Shot 2025-05-04 at 5 03 32 PM" src="https://github.com/user-attachments/assets/2536ac2e-a81c-4663-a660-97bb1fa4eb32" />
</p>
<p>
Open Windows PowerShell > type command "Get-FileHash" "the file location" (Can copy-paste the file location into the command-line) "the name of the file" and add -Algorithm MD5 to the end > Enter
</p>
<br />

<p>
<img width="1145" alt="Screen Shot 2025-05-04 at 5 07 01 PM" src="https://github.com/user-attachments/assets/f3615fe4-6a59-4070-9eb7-9422a37f8acd" />
</p>
<p>
Notice a Hash (a fixed length, alphanumeric string) has been created. Run the same command again (by either clicking the up-arrow on your key board or copy paste the previous command line and hit enter). See that the hash was produced again has not changed.
</p>
<br />

<p>
<img width="1142" alt="Screen Shot 2025-05-04 at 5 13 37 PM" src="https://github.com/user-attachments/assets/650e76b9-2c0b-47ae-841d-dff7ba559e71" />
</p>
<p>
Now go back to the Text Document (Md5sum.txt) created earlier and change the text content inside. Enter "Bye" instead of "Hello" for example > File > Save
</p>
<br />

<p>
<img width="856" alt="Screen Shot 2025-05-03 at 5 08 07 PM" src="https://github.com/user-attachments/assets/e01317a2-90db-4b4e-9ef2-1fd6daf16fea"/>
</p>
<p>
Return to the PowerShell command line and run the same previous command. Notice the hash produced is now different. Hashing is a method used to determine data integrity. The contents of a file are said be unaltered if the hash produced remains the same. If the hash changes, then the contents of the file have changed.
</p>
<br />
