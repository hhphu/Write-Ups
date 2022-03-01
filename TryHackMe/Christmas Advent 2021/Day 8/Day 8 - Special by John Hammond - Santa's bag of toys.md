**What operating system is Santa's laptop running ("OS Name")?**
	By going through the log in chronical order, I can easily figure the computer system in one of the log files
![[THM-Day8-Q1.png]]

-> Answer: Microsoft Windows 11 Pro

-------------

**What was the password set for the new "backdoor" account?**
	When investigating other logs, I noticed that the attacker created a second account with a backdoor
![[day8-q2.png]]

Here, the attacker used net commands to create a new user and add it to the administrators group.

> net user USER_NAME PASSWORD /add - create a new account with USERNAME and PASSWORD

> net localgroup GROUP_NAME USER_NAME /add - add the user account to a group

-> Answer: grinchstolechristmas

-------------------------------------
**In one of the transcription logs,  the bad actor interacts with the target under the new backdoor user account, and copies a unique file to the Desktop. Before it is copied to the Desktop, what is the full path of the original file?**
![[d8q3.png]]

-> Answer: C:\Users\santa\AppData\Local\Microsoft\Windows\UsrClass.dat

------------------------------

**The actor uses a [Living Off The Land](https://lolbas-project.github.io/lolbas/Binaries/Certutil/) binary (LOLbin) to encode this file, and then verifies it succeeded by viewing the output file. **What is the name of this LOLbin?****
![[d8q4.png]]

-> Answer: certutil.exe

-------------------------------

**Drill down into the folders and see if you can find anything that might indicate how we could better track down what this SantaRat really is. **What specific folder name clues us in that this might be publicly accessible software hosted on a code-sharing platform?**

-> Answer: .github

------------------------------

**Additionally, there is a unique folder named "Bag of Toys" on the Desktop! This must be where Santa prepares his collection of toys, and this is certainly sensitive data that the actor could have compromised. What is the name of the file found in this folder?** 

-> Answer: bags_of_toys.zip

------------------------------
**What is the name of the user that owns the SantaRat repository?**

-> Answer: Grinchiest

-------------------------------------------------
**Explore the other repositories that this user owns. What is the name of the repository that seems especially pertinent to our investigation?**

-> Answer: operation-bag-of-toys

-------------------------------
**Read the information presented in this repository. It seems as if the actor has, in fact, compromised and tampered with Santa's bag of toys! You can review the activity in the transcription logs. It looks as if the actor installed a special utility to collect and eventually exfiltrate the bag of toys. What is the name of the _executable_ that installed a unique utility the actor used to collect the bag of toys?

-> Answer: uharc-cmd-install.exe

------------------------------------
**Following this, the actor looks to have removed everything from the bag of toys, and added in new things like coal, mold, worms, and more! What are the contents of these "malicious" files (coal, mold, and all the others)?**

-> Answer: GRINCHMAS

-----------------------------
**What is the password to the original bag_of_toys.uha archive?**
I had to dig around the operation_of_bag repositories to find the password.

-> Answer: TheGrinchiestGrinchmasOfAll

-------------------
**How many original files were present in Santa's Bag of Toys?**

-> Answer: 228