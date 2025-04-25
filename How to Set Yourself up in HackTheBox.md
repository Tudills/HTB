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


---

### Step 2: Setting Up VirtualBox  
Lets go to 

[VirtualBox](https://www.virtualbox.org/)

<img src="![VirtualBox Org](https://github.com/user-attachments/assets/4e70dd96-e60f-4fb7-a631-387798bc7595)" alt="Alt Text" width="640" height="320"> 

Lets click the download link at the top of the page

![VirtualBox Org Download](https://github.com/user-attachments/assets/924cf6fc-7db9-4405-afcf-c43c605f9a02)


If we scroll down the page, we can see a list of choices where we can download an installer for VirtualBox for our respective Operating System.
In this case we are just going to click on the Windows Option.

![Virtual Box Org Picking Our Platform](https://github.com/user-attachments/assets/bc1edbc5-1264-41ed-a340-d7f8b702dea5)


After we downloaded it, let us go to the folder where our downloads are, and double click the installer.
Personally, When I installed VirtualBox I did a regular standard install. 
Literally clicked through all of the boxes. Straight Default.


---

### Step 3: Obtaining Kali  
Lets go get Kali
[Kali](https://www.kali.org)

![Kali Picking Download](https://github.com/user-attachments/assets/079c4f11-b0e2-4682-aa49-2606dff9e7af)

on the next page it will say, "Choose Your Platform"
we are going to click "Virtual Machines"

![Clicking Virtual Machine](https://github.com/user-attachments/assets/c9e1dd4d-538a-4cf8-9821-43de26505d3f)
photo 3.2***

Within the options we have to choose from, we are going to select *"VirtualBox"*

![Clicking Virtualbox Download](https://github.com/user-attachments/assets/8598bc72-9f32-400e-aef5-28b62c3d237d)

_Now this is going to take a minute. It's fairly large download._

Step 4: Optional ways to keep things tidy.

Typically on my Desktop, I'll make folder. Something like, _"Virtual Machines"_ or something of the like.

![Screenshot 2025-04-06 161726](https://github.com/user-attachments/assets/1ae6cc1a-7629-4e1b-819d-93b7f845cff4)

Within this folder I'll maker two subfolders, _"images"_ and _"snapshots"_.

![Screenshot 2025-04-06 161747](https://github.com/user-attachments/assets/13ad27c7-d13d-4c19-a529-48197148bdb4)


When my Kali Image has finished downloading. I'll put that bad boy in my images folder.

![Screenshot 2025-04-06 161845](https://github.com/user-attachments/assets/b1d82d55-330a-4cb9-baa7-6ebefe9a926b)

After I move the Zip file, I'll extract it. And usually trim the name.

![Screenshot 2025-04-06 162408](https://github.com/user-attachments/assets/eba73205-35ea-4740-bc8a-907299ebbc29)

_(I'll delete the zip file at this point honestly.)_

---

### Step 5: Reboot and Running a Kali VM

I would advise, once Virtual Box is installed and your kali image is downloaded, 
to Reboot your computer. Upon a successful reboot, open up VirtualBox. 
You'll see a couple of choices. "New" and "Add" we are gonna choose "Add" .

![VirtualBox Config](https://github.com/user-attachments/assets/018295d5-1b19-4b89-a15b-81b63261fb4a)


It will open up a browser window, where we can navigate to the image we downloaded earlier from Kali,
There will be a little blueish box.

![Screenshot 2025-04-06 162514](https://github.com/user-attachments/assets/9aca34b2-717f-4d13-968e-df1d81ff06db)


And that's what we will select. This is a preconfigured image, 
for now we aren't going to tamper with it too much.

---

### Step 6: "I'm In"

Kali is running, we are at a user log in, our default credentials are

_username: kali_
_password: kali_

![Screenshot 2025-04-06 163016](https://github.com/user-attachments/assets/a4de2988-7b6a-479d-868f-ab0132c3a671)

within kali we will click the terminal box.

![Screenshot 2025-04-06 165643](https://github.com/user-attachments/assets/9453ada8-2d22-4254-a006-e12b677fe8cf)

and run the initial Linux Commands

_sudo apt upgrade -y_
_sudo apt update_

![Screenshot 2025-04-06 163952](https://github.com/user-attachments/assets/d4d39483-f8a0-4be9-a82f-627368e2aa70)

It will ask for a password, which will be, _"kali"_ as stated above.

---

### Step 7: HTB; a primer

Open up firefox, and go to [HackTheBox](https://www.hackthebox.com) 
you'll see the icon at the top of the screen.

Which will open up a login option.

![Screenshot 2025-04-06 163514](https://github.com/user-attachments/assets/640ec484-3203-43e6-8100-ea982db5d1e9)

and from there, select the option on the right, which is "Hack the Box Labs"

![Screenshot 2025-04-06 163722](https://github.com/user-attachments/assets/22d8db1d-53d8-4a71-9d01-148197e8eec2)

In the left column of the page you will see, "Starting Point"
We will be going to that.

![HTB - Starting Point](https://github.com/user-attachments/assets/bda0731d-0e0b-4c91-96c3-b07ab8fa3ad1)


Now if we look to the top right of the screen, we see a section that says, "Connect to HTB" a box will expand.
With three options,
*"Machines"*
*"Starting Point"*
*"Seasonal"*

We are doing *"Starting Point"*
![Starting Point](https://github.com/user-attachments/assets/fde8c96a-76b2-43e4-9f91-c628c08747e7)


It will give you two options.
"Pwnbox"
"OpenVPN"

We are going to be selecting, "OpenVPN"

![Pwnbox and Openvpn](https://github.com/user-attachments/assets/cc355da1-3535-4945-9a98-7da54580134f)

The OpenVPN tab will provide you with two drop box choices, we are going to assume that we aren't
pay for HTB and are just testing it out. So we will pick the NON-VIP options. 
_(I have VIP, So in the picture I have them selected.)_

At the Bottom of the tab, you will see a box that says, "Download" after selecting your preferences, 
Click that download box bud.

![Openvpn configuration options](https://github.com/user-attachments/assets/6333fa29-240c-4802-b36c-833fc43e1fe9)

Now, what i will describe here is a brief aside.

When we, _"Downloaded"_ we did not download OpenVPN, what we downloaded was a user specific config file.
This file is going to have your user information. Basically that whole drop menu, and logging into our accounts,
and then finally clicking, download, we successfully made a configure file. If this doesn't make sense trust the process,
it will soon.

---

### Step 8: HTB or,  _"I'm in Pt.2: Electric Bugaloo."_

_Pop open that Terminal daddy_

Try typing the command, "ls" like "list" but "ls" _no quotes._

It's going to show you where you are currently in the directory of kalis file structure.

![Screenshot 2025-04-06 175553](https://github.com/user-attachments/assets/6b23e874-73b0-4e1b-9116-c64ff74a8370)

Now try typing, "cd Downloads" _no quotes_
Commands are case sensitive with Linux. So make sure you are giving it the "Big D" _quotes._

Notice how your command line prompt has changed, it's showing
"(kali@kali) - [~/Downloads]"
and that's because we are in the Downloads folder.

Type "ls" again. **No Quotes**

<img width="316" alt="NO WAY" src="https://github.com/user-attachments/assets/4653c035-9a0a-43b2-9b5f-0ad478707e4b" />

Look, our OpenVPN configure file!

let's try running it.

Type,
"sudo openvpn **starting_point_(your HTB user name should be here).ovpn" _No Quotes_

![Screenshot 2025-04-06 180805](https://github.com/user-attachments/assets/be1990e5-03af-4ac7-b051-9188deff0fe0)

What should happen is a wall of text will beat you over the head, this means openvpn is working.

If everything goes well, we should be able to look at our Hackthebox.com window... and we should see that icon from earlier change. _My laptop battery was becoming critically low at this point, But I chose to live life on the edge._

![Neat openvpn works](https://github.com/user-attachments/assets/256c5dba-d4de-48fb-8801-d1ea0f3ba30d)

Click, "File" in the terminal window, and select, "New tab".

![Screenshot 2025-04-06 180825](https://github.com/user-attachments/assets/a256f24c-94e7-408d-9321-7e2cda4de02b)

Notice now we have two tabs open the first one is running our openvpn, and now the second one is just in our download tab.
Let's change that, type "cd" in our new tab.

Let's open up the first HTB box in "starting point" at tier 0,
![HTB - Starting Point](https://github.com/user-attachments/assets/078c5a2a-2366-4cc2-9eab-39cff095d45f)

![Screenshot 2025-04-07 205424](https://github.com/user-attachments/assets/5df705cd-ac89-4303-b3ba-8cd27a0aed3a)

It should be called, _"Meow"_

![Screenshot 2025-04-07 205445](https://github.com/user-attachments/assets/a99e052d-ef2a-4595-a16b-d70818fc4ddf)

Notice how we can spawn an IP.
Let's do that. Click, "Spawn Machine" _This sometimes can take a moment._

![Screenshot 2025-04-07 205553](https://github.com/user-attachments/assets/05d24c43-2beb-40cb-aee6-245bb53002b8)


So the IP exists, and we are on HTBs virtual network. Theoretically, we should be able to make contact with the box.
Let's ping the IP just to make sure.

![Screenshot 2025-04-07 205840](https://github.com/user-attachments/assets/3f32bd4b-a1c5-49e9-82a4-8db33f8e08f6)


