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
<img width="1328" alt="Screen Shot" src="https://github.com/user-attachments/assets/c9a7a52f-b7e1-4436-95cf-c2e2ce21706b" />
</p>
<p>
Create a new file folder and name it "HashExample". Right-click the desktop > New > Folder
</p>
<br />

<p>
 <img width="1338" alt="Screen Shot 2025-05-04 at 4 12 08 PM" src="https://github.com/user-attachments/assets/86c90512-56c6-47db-8c46-b02bb79d14a7" />
</p>
<p>
Within this file folder, create a new text document. Right-click the "HashExample" folder> New> Text Document> Name the file "Md5sum" for example. Then enter in Type in a message, "Hello" for example.
</p>
<br />

<p>
<!--img width="1381" alt="01" src="https://github.com/user-attachments/assets/56dc32c2-d30d-4459-b58d-f1337cf99c41"-->
</p>
<p>
Open a command line in PowerShell and type command "Get - FileHash" along with the name of the text file you created. Notice a Hash (a fixed length, alphanumeric string) has been created. Run the same command again and see that the hash has not changed. 
</p>
<br />

<p>
<!--img width="1381" alt="01" src="https://github.com/user-attachments/assets/56dc32c2-d30d-4459-b58d-f1337cf99c41"-->
</p>
<p>
Go back to the etxt file that your created and change the text inside.... enter "Bye" instead of "Hello" for example. Save.
</p>
<br />

<p>
<img width="856" alt="Screen Shot 2025-05-03 at 5 08 07 PM" src="https://github.com/user-attachments/assets/e01317a2-90db-4b4e-9ef2-1fd6daf16fea"/>
</p>
<p>
Return to the command line and run the same command. Notice the hash produced is now different. Hashing is a method used to determine data integrity (CIA). The data is the same if the hashes are the same. If the Hashes ran at another point in time is different, then the data has changed.
</p>
<br />
