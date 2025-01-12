---
title: "Sudo"
date: 2021-11-09T15:12:13-06:00
draft: false
weight: 9
original_author: "Paul Matthews" 
reviewer: "" # to be set by the approving reviewer
last_editor: "" # update each time the file is edited
last_edit_date: # just the date is enough (don't worry about the time portion)
---

## The `sudo` command

The `sudo` command stands for **SU**bstitute **U**ser **D**o. It allows you to run any Bash command as a substitute user.

The `sudo` command is most *commonly used* to run a command as the **root** user that has full permissions to everything on the machine.

{{% notice note %}}
When using the `sudo` command to execute a command as a different user, your user must be in the `sudoers` file. **You will be prompted to enter your password to authenticate the user and execute a command as another user**. Ubuntu by default adds all new general users to the `sudoers` file. There is a `sudoer` bash command for managing the `sudoers` file. The `sudoer` file exists in the `/etc` directory.
{{% /notice %}}

Let's take a look at how to use the powerful `sudo` command.

### The `whoami` command

The `whoami` command simply displays the current user.

Go ahead and execute the `whoami` command:

![whoami](pictures/whoami.png)

This makes a lot of sense. We are the `student` user.

#### The `whoami` command as the daemon user

Run the same command this time as the `daemon` user.

Execute `sudo -u daemon whoami`:

![sudo -u daemon whoami](pictures/daemon-whoami.png)

You will be prompted to enter your password, which if you followed the configuration guide in this course should be **admin**. As you type **nothing will be displayed** on the terminal, this is a security feature so someone that can see your terminal will not know what your password is. After typing your password hit enter. Assuming your password was correct you should see the following:

![sudo -u daemon whoami results](pictures/daemon-whoami-results.png)

As we can see we ran the `whoami` command as the `daemon` user and so the display reads `daemon`.

#### The `whoami` command as the root user

Execute `sudo whoami`:

![sudo whoami](pictures/root-whoami.png)

The default for the `sudo` command is to execute the command as the `root` user.

## Using `sudo`

Running a command as the `root` user is sometimes necessary. You may need to read, or edit a file that your current user doesn't have read or write access to. However, the `root` user always has read, write, and execute access to all files. Making `sudo [command]` a very useful tool to have in your pocket.

As an example let's say we needed to read the contents of the mysterious `/etc/shadow` file.

![cat /etc/shadow](pictures/cat-etc-shadow.png)

Our `student` user doesn't have read access to this file. So we can run the same command as `root`.

![sudo cat /etc/shadow](pictures/sudo-cat-etc-shadow.png)

Running the command as the `root` user gave me read access to the file. General user's do not have read access to this file because the file lists **all** users and their hashed password.

You can see clearly that the `student` user's hashed password is: `$6$YQsJ8yJfzXt5L...`. 

{{% notice bonus %}}
A hashed password can be cracked using a rainbow table, which goes way outside the scope of this class. However, knowing that a hashed password can be cracked illustrates why general users **do not have access to read the `/etc/shadow` file**.
{{% /notice %}}