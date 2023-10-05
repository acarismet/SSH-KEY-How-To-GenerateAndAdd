# SSH-KEY-How-To-GenerateAndAdd

Easy Solid Steps To Generate and Add SSH Key

## Why We Need SSH Key and How It Works?

SSH Key saves you time by preventing you from having to log in with a password for every transaction on GitHub. With this key GitHub recognizes easily that the one is trying to do something is exactly you.
When you generate SSH Key, it creates two different keys. One of them is Private Key which stays in your device and other one Public Key which goes to GitHub. To use an analogy, Private Key is the lock keeps you safe and Public Key is the unique key for this lock. If two keys match GitHub defines authority for you.

## Step by Step Generating and Adding New SSH Key

1. We need a txt/doc etc. file and make sure that the folder containing this file will not be easily deleted and cannot be accessed. Create the text file with proper name e.g. ssh-key.

2. In the directory that contains your text file, open git bash here with right-click.

3. (Caution Don't Use CTRL+V to paste) Copy & paste this into Bash and press enter : ssh-keygen -t rsa -b 4096 -C "github" && cat ~/.ssh/id_rsa.pub

4. You'll see Bash will ask name of text file. Write the same name of your file exactly. And you'll see question(y/n) about existance of this file you'll enter y.

5. Then Bash will ask passphrase. Don't write anything. You will see that whatever key on keyboard you press you can't see anything so don't write. Copy and paste this to generate new passphrase and press enter:
   dd if=/dev/urandom bs=16 count=1 2>/dev/null | base64 | sed 's/=//g'

6. You'll get two keys and see a message that which key saved to which file. Go to file that contains public key(text.pub). You can see the key starting with letters like ssh-rsa and ending with Github, which is about 730 characters. Copy this Public Key. (In Linux it appears automatically on command line)

7. Open Github/Settings/SSH and GPG keys. Click New SSH key button. Write proper Title, make sure key type is Authentication Key and paste the Public Key to Key section. Click Add SSH Key button.

8. Congratulations You Got The SSH KEY...

9. Strongly Recommend Bonus: Please Enable Two-Factor Authentication(2FA) To Log In GitHub.
