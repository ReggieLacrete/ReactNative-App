React Native App Project

2 Simple steps to make my app work 👇🏾👇🏾👇🏾

First, Open a bash terminal in the json-server/ folder by following the
instructions below:
While it's possible to do this in VS Code, i recommend you use Git Bash (Windows) or Terminal (macOS) for this purpose to keep the server separate from your React client application. 
In macOS, you can right click on the json-server folder, then choose Services -> New Terminal at Folder.
In Windows, you can right click on the json-server folder from Windows File Explorer, then choose Git Bash Here.
If the above options do not work for you, you can open Git Bash or Terminal then use the cd command to navigate to the json-server/ folder. Assuming your NucampFolder is on your Desktop, and you created the json-server/ folder in the NucampFolder as previously instructed, you can use this command:
cd ~/Desktop/NucampFolder/json-server
Once you have a bash terminal open to the json-server/ folder, enter the ls command and confirm that you see the public/ folder and the db.json file listed: $ 1s
db.json public/

Now enter this command in your bash terminal: 
json-server -H 0.0.0.0 --watch db.json -p 3001 -d 2000
The above command starts json-server, After you enter the above command, your terminal should look similar to this. You should see the campsites, comments, partners, promotions, and feedback resources listed as shown below:

    \{^_^}/ hi!
Loading db.json
Done
Resources
http://0.0.0.0:3001/campsites
http://0.0.0.0:3001/comments
http://0.0.0.0:3001/partners
http://0.0.0.0:3001/promotions
http://0.0.0.0:3001/feedback
Home
http://0.0.0.0:3001
Type s + enter at any time to create a snapshot of the database
Watching.

Secondly, find out the IP address of your computer:
In macOS, go to System Preferences->Network to find the IP address of your network adapter.
In Windows, you can use the instructions available at https://www.digitalcitizen.life/find-ip-address-windows to find your machine's IP address. Note: The ipconfig command shown in the instructions can be used from Git Bash. Look for the IPv4 address, not the IPv6. 
Next, edit the file named baseUrl.js in the shared/ folder and edit the following to it:
export const baseUrl = 'http://<Your Computer's IP address>:3001/';
For example, if your IP address is 192.168.1.121, then the above line should be as follows:
export const baseUrl = 'http://192.168.1.121:3001/';
Don't miss that ending slash after 3001! It's a small but very important detail.



<h2>About the project</h2>

<p>This is a e-commerce website built with React and CSS. This
website features a modern and intuitive design, with easy-to-use navigation and a
simple shopping experience that puts the focus on the products.</p>

<h3>Build with:</h3>

» Vanila CSS <br>
» React JS

<h2>Screenshots of the Project 📸</h2>
<br>
<h3 align='center'>Home Page 🏡</h3>

<div align='center'>
<img src='https://github.com/ReggieLacrete/ReactNative-App/assets/133793148/8260f3a4-532f-454b-baa3-0a8263da7e52'/>
</div>
<br><br>
<h3 align='center'>Login Page 👇</h3>
<div align='center'>
<img src='https://github.com/ReggieLacrete/ReactNative-App/assets/133793148/2e49bca0-1fa5-4694-8467-2635ec671ca9'/>
<br>
<br>
<h3 align='center'>Campsite Directory 🌲</h3>

<div align='center'>
<img src='https://github.com/ReggieLacrete/ReactNative-App/assets/133793148/bcd5889a-a6d0-4c7f-8857-14a105e0bd0d'/>

<br>
<br>
<h3 align='center'>Reservation Search 🔎</h3>

<div align='center'>
<img src='https://github.com/ReggieLacrete/ReactNative-App/assets/133793148/72dee16d-6253-4a3a-9dc7-b80a9cefd6f3'/>
</div>
