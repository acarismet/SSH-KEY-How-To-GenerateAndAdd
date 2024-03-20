# SSH Key | How To Generate And Add

**_Easy Solid Steps To Generate and Add SSH Key_**

> Please make sure that the same commands are valid for the command lines of non-Microsoft operating systems. For example, I got my own SSH key by taking these commands from Linux commands.

## Why We Need SSH Key and How It Works?

**SSH Key** saves your time by preventing you from having to log in with a password for every transaction on GitHub. With this key GitHub recognizes easily that the one is trying to do something is exactly you.
When you generate **SSH Key**, it creates two different keys. One of them is **Private Key** which stays in your device and other one **Public Key** which goes to GitHub. To use an analogy, **Private Key** is the lock keeps you safe and **Public Key** is the unique key for this lock. If two keys match GitHub defines authority for you.

## Step by Step Generating and Adding New SSH Key

1. We need a _txt/doc_ etc. file and make sure that the directory containing this file will not be easily deleted and cannot be accessed. Create the _text file_ with **proper name** e.g. ssh-key.

2. In the directory that contains your text file, open **git bash here** with _right-click_.

3. (**Caution:** Don't Use `CTRL+V` to paste) Copy & paste this into _Bash_ and press enter :
   `ssh-keygen -t rsa -b 4096 -C "github" && cat ~/.ssh/id_rsa.pub`

4. You'll see Bash will ask name of text file. Write the same name of your file exactly. And you'll see question`(y/n)` about existance of this file you'll enter `y`.

5. Then Bash will ask `passphrase`. Don't write anything. You will see that whatever key on keyboard you press you can't see anything so don't write. Copy and paste this to generate new `passphrase` and press enter:

   `dd if=/dev/urandom bs=16 count=1 2>/dev/null | base64 | sed 's/=//g'`

6. You'll get two keys and see a message that which key saved to which file. Go to file that contains **Public Key**(text.pub). You can see the key starting with letters like _ssh-rsa_ and ending with _Github_, which is about 730 characters. Copy this **Public Key**. (In Linux it appears automatically on command line)

7. Open _Github/Settings/SSH and GPG keys_. Click _New SSH key_ button. Write proper _Title_, make sure _key type_ is _Authentication Key_ and paste the **Public Key** to _Key_ section. Click _Add SSH Key_ button.

8. Congratulations You Got The **_SSH KEY_**...

9. Strongly Recommend Bonus: Please Enable **Two-Factor Authentication(2FA)** To Log In GitHub.

## How To Use SSH Key?

\*I assume that you've completed previous steps above and had the **SSH Key.\***

1. You can use your **SSH Key** to pull and clone existing/new project from your GitHub Repositories.

   > _If you have question about what is difference between cloning HTTPS and cloning SSH Key from Github you can check Clone-Differences.md file in this repo._

2. Go to Github.com or desktop app. Its up you to get SSH Key from existing repository or new one. Either way in repo page you'll see green _< >Code button_ in the upper right corner. Under _Local_ click _SSH_. Copy that key.

3. Open Bash in the directory where you want to place the file, or navigate to that directory with commands.

4. Paste the SSH Key you copied here as follows and press enter:
   `git clone your ssh key`

5. When you don't recognize any term here please go to [git documentation](https://git-scm.com) and search in its search bar. And thanks to AI, you can limitless questions to gpt services about how to use Git and GitHub.

---

> **If you were able to benefit from this information or found it useful, do not forget to star it and share it with your friends who are new to software development. :)**
