Run Postman Colletion in Jenkins 

Q.1. How to install Jenkins ?
Prerequisites:-
1. Hardware requirements: You need minimum 256 MB of RAM in your computer or laptop to install Jenkins & You need at least 1 GB of space in your hard drive for Jenkins.
2. Software Requirements: Since Jenkins runs on Java, you need either latest version of Java Development Kit (JDK) or Java Runtime Environment (JRE).
3. Release Types : Jenkins releases two types of versions based on the organization needs.
-Long term support release (LTS) :
Long-term support releases are available every 12 weeks. They are stable and are widely tested. This release is intended for end users.
-Weekly release:
Weekly releases are made available every week by fixing bugs in its earlier version. These releases are intended towards plugin developers.
4. Download& Setup 
Step 1) Got to https://www.jenkins.io/download/ and select the platform.
Step 2) Go to download location from local computer and unzip the downloaded package. Double-click on unzipped jenkins.msi. You can also Jenkin using a WAR (Web application ARchive) but that is not recommended.
Step 3) In the Jenkin Setup screen, click Next.
Step 4) Choose the location where you want to have the Jenkins instance installed (default location is C:\Program Files (x86)\Jenkins), then click on Next button.
Step 5)Click on the Install button.
Step 7) During the installation process an info panel may pop-up to inform the user that for a complete setup, the system should be rebooted at the end of the current installation. Click on OK button when the Info panel is popping-up:

Note : We will using Long Term Support. 
![image](https://github.com/Ka-4517/API-Testing-Details/assets/72380607/107d2d02-5670-4715-af37-5d6f6ede5e28)


![image](https://github.com/Ka-4517/API-Testing-Details/assets/72380607/ccce1068-329a-45d8-a078-4959817ecd61)


![image](https://github.com/Ka-4517/API-Testing-Details/assets/72380607/62b2d057-f3b8-4815-aa38-7deb2c0f4e5e)

![image](https://github.com/Ka-4517/API-Testing-Details/assets/72380607/c214fb7c-ae49-4649-9378-4a7c69d2a708)
 Enter this Password in your Localhost page.

 Now : 1. Click to Configure Proxy 
       2. Click Install Suggested Plugins  >>
       ![image](https://github.com/Ka-4517/API-Testing-Details/assets/72380607/76c98059-08eb-46e2-b4af-3651ebdee1a2)

       3. Create Admin User & Password >>
       ![image](https://github.com/Ka-4517/API-Testing-Details/assets/72380607/714a00c5-3b4e-48cd-ae7d-2a153c42d24d)
       User id : admin123
       password : admin
       Full Name : Karan Gupta
       email : karangupta4517@gmail.com
       

       4. Click on Save & continue >>
       5. Now you will see This Page 

       ![image](https://github.com/Ka-4517/API-Testing-Details/assets/72380607/cd4d8e42-86cc-4fea-a90c-4dac51d46770)
       

       Paste this URL to browser 
       Click to Save & Finish Button >> you will get jenkins ready 

       Click on Start Using Jenkins Button <<< 
       ![image](https://github.com/Ka-4517/API-Testing-Details/assets/72380607/a90f7955-e2d1-456e-bde8-7736bca52a1e)
       

       
       -------------------------------------------------------------------------------------------------------------------------------------------------------
       


Q.2. How to Run postman collection from jenkins ?
- Bat File having this code & need to add this in jenkins build set : newman run "C:\Users\Karan\Desktop\Postman\BookingAPI\Booking_API.json -e C:\Users\Karan\Desktop\Postman\BookingAPI\environment.json"
- Run Fron Jenkins
- New Item >>. select Freestyle project >> Ok >> Give path in build setup of the bat file
- Generate build 

-How to solve this issue ?  >> ![image](https://github.com/Ka-4517/API-Testing-Details/assets/72380607/9147bbde-9f49-4195-b550-140e3105f858)
ANS: Now go to that bat file and change the text with this : 
newman run --disable-unicode C:\Users\Karan\Desktop\Postman\BookingAPI\Booking_API.json -e C:\Users\Karan\Desktop\Postman\BookingAPI\environment.json (For me this is not working)

"
output_with_color = "[90m┌─────────────────────────[39m[90m┬────────────────────[39m[90m┬────────────────────┐[39m"
output_without_color = remove_ansi_escape_sequences(output_with_color)
Just do this 
![image](https://github.com/Ka-4517/API-Testing-Details/assets/72380607/97d04e5b-00c2-4aae-90a0-71e60e257fae)

![image](https://github.com/Ka-4517/API-Testing-Details/assets/72380607/a5aa294b-faa9-4fc8-94b1-f40f278d6422)


"

If You have exe jankins then / this is not work then : do these :- C:\Users\Karan\.jenkins (For me this is not working)
1. Go to your Jenkins installation directory and open the Jenkins XML file.
2. Add the highlighted text(-Dfile.encoding=UTF-8) ![image](https://github.com/Ka-4517/API-Testing-Details/assets/72380607/4a02df29-0d28-4085-b1eb-cddf843bc024)
 and save.
3. Open Command Prompt -->Go to your Jenkins installation directory and enter the command to stop Jenkins :- jenkins.exe stop
4. Restart jenkins by entering the command at the command prompt:- jenkins.exe restart
5. Re-run build in jenkins and check the console output. https://prnt.sc/zoi3BmOAcKQ5

Q.3. How to set CRON pattern?


Q.4. How to generate newman advance html report in Jenkins?


