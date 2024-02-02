## Setting a Honeypot In Kali Linux Using PentBox

Welcome to a hands-on exploration of setting up a honeypot on Kali Linux using Pentbox! In this lab project, I will guide you through the step-by-step process and protocols I employed to create an effective honeypot environment.

## Getting Started

Before we dive done to the neety grity the importance of setting up a honeypot on your server root account can't be emphasized. The reason so is that it helps create an environment that truly mirrors real-world systems, making it appealing to attackers looking for extensive control. 

By configuring it this way, we can gather detailed information about various attack strategies, gain insights into how attackers escalate their privileges and stay abreast of the ever-changing tactics employed in the realm of cyber threats 

1. let's get into our root account.
  Use this command and type in your password 
  ```bash
  su
   ```
![image](https://github.com/jduru213/Linux-Projects-/assets/112328773/cb21c481-7e0a-4815-b1b9-27f5f739020e)

2. Once in your root account, open Chrome on your web browser and paste the link below, then clone the repository code

###### Original code by Technical Dada
###### Source: https://github.com/technicaldada/pentbox

![image](https://github.com/jduru213/Linux-Projects-/assets/112328773/1c7064bf-3a7f-4d37-8afe-47b2f6acbcac)

![image](https://github.com/jduru213/Linux-Projects-/assets/112328773/32aa6f11-ac88-45e8-95f0-c73a9a246a12)


### Step 1: Cloning the code into the terminal 
- Next, in your terminal use the "ls" command to find folders and the "cd" command to navigate and open the folder you would like to use. 
- Then clone the repository into the desired folder 

![image](https://github.com/jduru213/Linux-Projects-/assets/112328773/37afbc5a-1742-43ef-8ae4-60196003402c)

## Step 2: Find the File and Unzip
Once in the directory of PentBox, to unzip the file 
use:
 ```bash
  tar -zxvf pentbox.tar.gz 
 ```
![image](https://github.com/jduru213/Linux-Projects-/assets/112328773/4568ad86-78db-487f-bf2c-a30f3d7737bd)

## Step 3: Open file and Run tool 
Once you have unzipped it's time to open and run this file! 

1. To open the latest and most recent tool on the file: 
```bash
cd pentbox-1.8/
 ```
2. To run the tool:
   ```bash
   ./pentbox.rb
    ```
   ![image](https://github.com/jduru213/Linux-Projects-/assets/112328773/4b88458d-6757-4c65-a263-49f6b643862f)

- After running the following commands, it should bring you to a menu with options to select from. Now since we plan on configuring a honeypot it's important to include network tools in your configuration, With network tools, you can see who's trying to interact with it, what methods they're using, and if they're trying to exploit any weaknesses. Therefore we'll select option 2 (Network tools)
- Then Option 3 (honeypot)
  
Two other options should appear stating either: Fast Auto Configuration or Manual Configuration
- For now, we'll start with Fast Auto Configuration 
  
## Step 4: Obtaining our IP address 
- Knowing your IP address is essential when setting up a honeypot for a few key reasons.

- First, it allows you to configure the honeypot to mimic a real system, as attackers typically target specific IP addresses. Secondly, it helps in monitoring and logging providing insight on attack patterns. We can also 

- To obtain and figure out our IP address open another terminal and use this command:
 ```bash
   ifconfig 
 ```
![image](https://github.com/jduru213/Linux-Projects-/assets/112328773/cfb5153e-d866-44d2-a377-b262bc7be7c0)

## Step 5: Let's put it to the Test!

- Now it is time to test it! Open your Chrome browser and paste your IP address 

![image](https://github.com/jduru213/Linux-Projects-/assets/112328773/9571a16e-49aa-4a12-b181-8218b59146b0)

- Should bring you to a page stating the Access was denied and the IP address login failed 
  
 ![image](https://github.com/jduru213/Linux-Projects-/assets/112328773/d5b75f6c-cda9-41e0-9b3c-344cab4c4366)

- Now let's go now and check our honeypot. You should see an IDS (Intrusion Detection System)  message alerting you about the attempt, the port it is operating on, and the IP address it's coming from.

![image](https://github.com/jduru213/Linux-Projects-/assets/112328773/76e93dd4-02bb-4417-b098-67d5af42e505)


## Step 6: Testing from a different server 
Let's test it out from outside the server using Parrot OS by pinging the IP address found on your Kali Linux terminal.

* Note: If you don't have Parrot OS, you can still use your regular web browser

1. Pinging our IP addresses

Purpose - Pinging the IP address of your honeypot on Parrot OS is crucial to ensure basic network connectivity. It helps verify reachability, validate network configuration, and serves as an initial test to check if the honeypot responds to basic requests. 
   
 ![image](https://github.com/jduru213/Linux-Projects-/assets/112328773/253f82c4-5d7c-4a1d-b012-44b143ef2ae0)
 * Enter ctrl C to fast-forward the purpose 

2. After pinging the IP address, find the iP address of the Parrot OS by opening another terminal and using the ifconfig command
   
![image](https://github.com/jduru213/Linux-Projects-/assets/112328773/3a3522ce-dfc7-46e3-9d82-4561c280c49f)
   
3. Paste your IP address found on Kali Linux into your web browser

![image](https://github.com/jduru213/Linux-Projects-/assets/112328773/a4cb476a-ce57-4f3e-a354-dac0adfa74e8)

4. You should then see the honeypot on your Kali Linux server detecting an intrusion attempt and proving where the attack is coming from 

![image](https://github.com/jduru213/Linux-Projects-/assets/112328773/4526aaa5-2db1-4605-8b66-e8bbba9c5f49)

## Step 7: Manual Configuration 
Now lets say that we decide to mually confgure our honeypot. 

- Enter the port number you would like, I personally decided to use port 23 (telnet)
- Insert a false mesage you will like to display after dectection
- Save the log file

 - Here is my example:
![image](https://github.com/jduru213/Linux-Projects-/assets/112328773/c95ddb71-e39b-4187-b653-3bf3a9d1ea54)

- Since we are using port 23 which is telnet enter the following into your operating system 
* Note: The same IP address you obtained on your kali linux server, copy and paste it 

![image](https://github.com/jduru213/Linux-Projects-/assets/112328773/3090d6a5-c408-4457-a0de-e7375840d5af)

- Now if we go back to our honeypot set on Kali linux, you should see an dectection alert 
![image](https://github.com/jduru213/Linux-Projects-/assets/112328773/04760bfd-5545-4b79-bdbc-debc37bb8cd4)

## Conclusion: 

- Setting up a honeypot on Kali Linux using PentBox was quite useful for me as a student. It provided a hands-on opportunity to apply academic knowledge in a real-world cybersecurity scenario. Configuring the honeypot provided me with useful insights into the complexity of building a simulated environment that attracts and monitors potential cyber threats. 

