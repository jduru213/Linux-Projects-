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

2. Once in your root account, open Chrome on your web browser and paste the link below, then  clone the repository code 
   
### Original code by Technical Dada
### Source: https://github.com/technicaldada/pentbox

[image1](https://raw.githubusercontent.com/jduru213/Linux-Projects-/main/assets/112328773/314589a6-c1f0-4842-acab-9b4fb7f5399b.jpg =300x)
[image2](https://raw.githubusercontent.com/jduru213/Linux-Projects-/main/assets/112328773/db599b7c-cf33-4141-bb73-96de849f6156.jpg =300x)

### Step 1: Cloning the code into terminal 
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
Once you have unzipped the file use the following commands
1. This is too open the latest and most recent tool 
```bash
cd pentbox-1.8/
 ```
2. This is to run the tool
   ```bash
   ./pentbox.rb
    ```
   ![image](https://github.com/jduru213/Linux-Projects-/assets/112328773/4b88458d-6757-4c65-a263-49f6b643862f)

After running the following commands, should bring you to a menu with options to select from. Now since we plan on configung a honeypot... select option 2 (Network tools) 
Then Option 3 (honeypot)
why should we seletc netwrok tools if we are confifgurng a honeypot 
   
## Step 4: Fast Auto configuration 

## Using SAM CLI with AWS Cloud9
