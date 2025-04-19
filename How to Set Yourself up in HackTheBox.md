# How to set yourself up in HackTheBox

**Author**: Tudills  
**Date**: 2025-04-18  


---

## Overview

Quite Simply, This tutorial is going to help you set up a virtual machine, Configure it, and help you along the way of getting set up on 

---

## Requirements

- Computer
- Pulse (e.g., VS Code)
- Browser
- Trouble Shooting Skills

---

## VirtualBox Guide

### Step 1: Making sure we can virtualize.
_You may not have to do this, depending on the settings of your computer_
  
Before we get started with setting up any virtualization, we need to make sure our computer supports it. This is fairly simple.
Turn off your computer, when you turn it back on repeatedly hit f2 or f12 or f10 or esc the manufacturer of your computer will 
determine which key it is. But it will most likely be one of those keys.
The goal here is to get into your computer's bios, What we are looking for is something called the BIOS/UEFI setup
There will be a setting within the BIOS, "CPU Configuration" or "Advanced" or "Security Settings"
Within one of the tabs in your BIOS, you will find an option that says "Virtualization" or "Virtualization Settings" 
or "Intel Virtualization Technology" or "AMD-V" or "SVM Mode" and make sure that this option is enabled.

After that is done, Save the changes and exit the BIOS/UEFI


![Step 1] ***placeholder for photo 1***

---

### Step 2: Setting Up VirtualBox  
Lets go to 
[VirtualBox](https://www.virtualbox.org/)


![Step 2.1]***placeholder for photo 2.1***

Lets click the download link at the top of the page

![Step 2.2]***placeholder for photo 2.2***


If we scroll down the page, we can see a list of choices where we can download an installer for VirtualBox for our respective Operating System.
In this case we are just going to click on the Windows Option.

![Step 2.3]***placeholder for photo 2.3***

After we downloaded it, let us go to the folder where our downloads are, and double click the installer.
Personally, When I installed VirtualBox I did a regular standard install. 
Literally clicked through all of the boxes. Straight Default.


---

### Step 3: Obtaining Kali  
Lets go get Kali
[Kali](https://www.kali.org)

![Step 3.1]***placeholder for photo 3.1***

on the next page it will say, "Choose Your Platform"
we are going to click "Virtual Machines"

![Step 3.2]***placeholder for photo 3.2***

Within the options we have to choose from, we are going to select *"VirtualBox"*

![Step 3.3]***placeholder for photo 3.3***

_Now this is going to take a minute. It's fairly large download._

Step 4: Optional ways to keep things tidy.

Typically on my Desktop, I'll make folder. Something like, _"Virtual Machines"_ or something of the like.

![Step 4.1]***placeholder for photo 4.1***

Within this folder I'll maker two subfolders, _"images"_ and _"snapshots"_.

![Step 4.2]***placeholder for photo 4.2***

When my Kali Image has finished downloading. I'll put that bad boy in my images folder.

![Step 4.3]***placeholder for photo 4.3***

After I move the Zip file, I'll extract it. And usually trim the name.

![Step 4.4]***placeholder for photo 4.4***
_(I'll delete the zip file at this point honestly.)_

---

### Step 5: Reboot and Running a Kali VM

I would advise, once Virtual Box is installed and your kali image is downloaded, 
to Reboot your computer. Upon a successful reboot, open up VirtualBox. 
You'll see a couple of choices. "New" and "Add" we are gonna choose "Add" .

![Step 5.1]***placeholder for photo 5.1***

It will open up a browser window, where we can navigate to the image we downloaded earlier from Kali,
There will be a little blueish box.

![Step 5.2]***placeholder for photo 5.2***

And that's what we will select. This is a preconfigured image, 
for now we aren't going to tamper with it too much.

---

### Step 6: "I'm In"

Kali is running, we are at a user log in, our default credentials are

_username: kali_
_password: kali_

![Step6.1]***placeholder for photo 6.1***

within kali we will click the terminal box.

![Step 6.2]***placeholder for photo 6.2***

and run the initial Linux Commands

_sudo apt upgrade -y_
_sudo apt update_

![Step 6.3]***placeholder for photo 6.3***

It will ask for a password, which will be, _"kali"_ as stated above.

---

### Step 7: HTB; a primer

Open up firefox, and go to [HackTheBox](https://www.hackthebox.com) 
you'll see the icon at the top of the screen.

Which will open up a login option.

![Step 7.1]***placeholder for photo 7.1***

and from there, select the option on the right, which is "Hack the Box Labs"

![Step 7.2]***placeholder for photo 7.2***

In the left column of the page yoiu will see, "Starting Point"
We will be going to that.

![Step 7.3]***placeholder for photo 7.3***

Now if we look to the top right of the screen, we see a section that says, "Connect to HTB" a box will expand.
With three options,
*"Machines"*
*"Starting Point"*
*"Seasonal"*

We are doing *"Starting Point"*

![Step 7.4]***placeholder for 7.4***

It will give you two options.
"Pwnbox"
"OpenVPN"

We are going to be selecting, "OpenVPN"
![Step 7.5]***placeholder for 7.5***

The OpenVPN tab will provide you with two drop box choices, we are going to assume that we aren't
pay for HTB and are just testing it out. So we will pick the NON-VIP options. 
_(I have VIP, So in the picture I have them selected.)_

At the Bottom of the tab, you will see a box that says, "Download" after selecting your preferences, 
Click that download box bud.

![Step 7.6]***placeholder for 7.6***

Now, what i will describe here is a brief aside.

When we, _"Downloaded"_ we did not download OpenVPN, what we downloaded was a user specific config file.
This file is going to have your user information. Basically that whole drop menu, and logging into our accounts,
and then finally clicking, download, we successfully made a configure file. If this doesn't make sense trust the process,
it will soon.

---

### Step 8: HTB or,  _"I'm in Pt.2: Electric Bugaloo."_

_Pop open that command line daddy_

![Step 8.1]***placeholder for 8.1***

Try typing the command, "ls" like "list" but "ls" _no quotes._

It's going to show you where you are currently in the directory of kalis file structure.

![Step 8.2]***placeholder for 8.2***

Now try typing, "cd Downloads" _no quotes_
Commands are case sensitive with Linux. So make sure you are giving it the "Big D" _quotes._

Notice how your command line prompt has changed, it's showing
"(kali@kali) - [~/Downloads]"
and that's because we are in the Downloads folder.

Type "ls" again. **No Quotes**

![Step 8.3]***placeholder for 8.3***

Look, our OpenVPN configure file!

let's try running it.

Type,
"sudo openvpn **starting_point_(your HTB user name should be here).ovpn" _No Quotes_

![Step 8.4]***placeholder for 8.4***

What should happen is a wall of text will beat you over the head, this means openvpn is working.

If everything goes well, we should be able to look at our Hackthebox.com window... and we should see that icon from earlier change. _My laptop battery was becoming critically low at this point, But I chose to live life on the edge._

![Step 8.5]***placeholder for 8.5***

Click, "File" in the terminal window, and select, "New tab".

![Step 8.6]***placeholder for 8.6***

Notice now we have two tabs open the first one is running our openvpn, and now the second one is just in our download tab.
Let's change that, type "cd" in our new tab.

![Step 8.7]***placeholder for 8.7***

This is what our terminal window tabs should now look like. 
One is running openvpn in our Download folder using the configuration openvpn file we downloaded. 
And this new tab is at the user end of the hard drive.

Let's open up the first HTB box in "starting point" at tier 0,
![Step 8.8]***placeholder for 8.8***

It should be called, _"Meow"_
![Step 8.9]***placeholder for 8.9***

Notice how we can spawn an IP.
Let's do that. Click, "Spawn Machine" _This sometimes can take a moment._

![Step 8.10]***placeholder for 8.10***

So the IP exists, and we are on HTBs virtual network. Theoretically, we should be able to make contact with the box.
Let's ping the IP just to make sure.

![Step 8.11]***placeholder for 8.11***

