---
title: "Configuration: VirtualBox"
draft: false
weight: 1
original_author: "Paul Matthews" 
reviewer: "" # to be set by the approving reviewer
last_editor: "" # update each time the file is edited
last_edit_date: # just the date is enough (don't worry about the time portion)
---

## VirtualBox

This configuration will walk you through the steps of downloading and installing [Oracle VM VirtualBox](https://www.virtualbox.org/).

VirtualBox is a *virtualization* tool. It will allow you to create a virtual operating system inside of your host operating system. Using this tool we will be able to begin working with a Linux Operating System inside of your personal operating system without compromising the integrity of your current Operating System. VirtualBox will handle all the implementation details and will create a isolated sandbox environment with the guest Linux Operating System.

## Downloading

First up we need to download the VirtualBox software onto our host machine.

At the time of writing VirtualBox 6.1 is the Oracle recommended version, however we recommend using the currently recommended version when you are downloading VirtualBox. See the following picture as an example.

![VirtualBox Homepage](./images/virtualbox-homepage.png)

Clicking the giant blue button stating `Download VirtualBox 6.1` should lead you to the [downloads page](https://www.virtualbox.org/wiki/Downloads) which has links for many common Operating Systems. The downloads page should like the following image.

![VirtualBox Downloads](./images/virtualbox-downloads.png)

On this page you should see multiple links that coincide with your Operating System. Upon clicking one of these links it should automatically start a download that will work for your OS.

{{% notice note %}}
If you are using a Linux based operating system the link from the downloads page will take you to another page with various options, find the one for your specific distribution.
{{% /notice %}}



### MacOS - Instructions

{{% expand "Click here to expand MacOS instructions" %}}

#### MacOS - Download

The direct link for the MacOS VirtualBox download can be found [here](https://download.virtualbox.org/virtualbox/6.1.28/VirtualBox-6.1.28-147628-OSX.dmg).

{{% notice warning %}}
The link will start a download for the **.dmg** file needed to install VirtualBox on a MacOS system.
{{% /notice %}}

{{% /expand %}}

### Windows - Instructions

{{% expand "Click here to expand Windows instructions" %}}

#### Windows - Download

The direct link for the Windows VirtualBox download can be found [here](https://download.virtualbox.org/virtualbox/6.1.28/VirtualBox-6.1.28-147628-Win.exe)

{{% notice warning %}}
The link will start a download for the **.exe** file needed to install VirtualBox on a Windows system.
{{% /notice %}}