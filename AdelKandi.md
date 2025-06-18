## CST 8254 Practical Mid Term

**Your Name:**

```
Adel Kandi
StudentID : 041182998
```


Using ``scp`` , send a copy of the file to your raspberry pi in the home folder. **What command did you use?**

**1.**

```
PS C:\Users\adelk> scp C:\Users\adelk\OneDrive\Documents\College\'Level 2'\'Network Administration'\AdelKandi.txt pi@100.92.198.123:/home/pi/
```

Open a **`putty/ssh`** session to your raspberry pi .

**2. What command do you use to see a directory listing that includes the permissions of the files?**

```
ls -l
```

Redo the last command and save the output of the command to a file **`pr1.txt`**. **What command did you use?**

**3.**

```
pi@adelpi:~ $ ls -l > pr1.txt
```

**4. What are the permissions of the file you just created?**

```
-rw-r--r--
```

**5. What command do you use to display the folder you are currently working from?**

```
pwd
```

Change the permissions of the file so that group members can only execute it. **What command did you use?** 

**6.**

```
chmod g=x pr1.txt
```

Create a folder **`midtermExam-SectionNumber`** under the current working directory of your raspberry pi. **SectionNumber** must be replaced with your lab section number (for instance Jérôme's Lab students  use 301).  **What command did you use?**

**7.**

```
mkdir midtermExam-301
```

**8. What are the permissions of this new folder  ?**

```
drwxr-xr-x
```

**9. What command do you use to list the ports your raspberry pi is listening to? Try it using the `-at` flag.**

```
netstat -at
```

Redo the last command saving the output of the command to a file **`pr2.txt `**. **What command did you use?**

**10.**

```
pi@adelpi:~ $ netstat -at > pr2.txt
```

On your laptop create a text file **`midtermPi.txt`**. The content of the file is a line stating that you were there. For instance mine would read: `**Jerome Mizon was there.**` Save the file.

From the command line start a sFTP session to your raspberry PI . **What command did you use to connect?**

**11.**

```
PS C:\Users\adelk> sftp pi@100.92.198.123
after that the results are: 
pi@100.92.198.123's password:
Connected to 100.92.198.123.
```

Copy the file **`midtermPi.txt`** to your PI using sFtp. **What command did you use?** 

**12.**

```
put midtermPi.txt /home/pi
```

On your PI  run the following command

```
pwd>mt.txt;tree -l>>pr.txt
```

**13.** What does the command do?

```
The command runs pwd command then saves the results on file called mt.txt, and for tree-l also it runs the command  and then saves resultsit on file called pr.txt
```

Using `useradd`, create a user named after you using the concatenation of your firstname and last name. **What command did you use?**

**14.**

```
sudo adduser adelkandi
```

Create the home directory for the user you just created and change the ownership of this folder to the user himself/herself. **What commands did you use?**

 **15.**

```
Well I found out that its already been created /home/adelkandi and permission is already set to only adelkandi 'pi@adelpi:/home $ ls -ld /home/adelkandi
drwx------ 2 adelkandi adelkandi 4096 Jun 18 11:26 /home/adelkandi' but if it did'nt i will do :
sudo mkdir /home/adelkandi
sudo chown adelkandi:adelkandi /home/adelkandi
```

Update your PI package list using `apt-get` , then use `apt-get` to install `Filezilla` on your  PI. **What commands did you use?**

**16.**

```
sudo apt update
sudo apt-get install filezilla

```

**17.** issue the following command on your pi:

`cd /home`

`ls -als > /home/pi/pr3.txt`


