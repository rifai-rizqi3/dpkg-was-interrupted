# dpkg-was-interrupted
How to fix “dpkg was interrupted, you must manually run sudo dpkg –configure -a to correct the problem” error.


Whether you are a beginner or a pro, if you have been using Linux or Nginx for WordPress then it may be common to see the error when you try to install apt-get or using apt or doing just a Yum Update. And believe me, it can be very frustrating when it occurs as you are restricted to install or update your software packages on WordPress using Linux. Now, this error can occur for anyone and is not only restricted to some of you using Amazon EC2, AWS Lightsail, or your traditional LAMP or XAMPP.

Don’t worry, we have got you covered.  Just run the following commands and tada!

```
sudo rm /var/lib/apt/lists/lock
```
```
sudo rm /var/cache/apt/archives/lock
```
```
cd /var/lib/dpkg/updates
```
```
sudo rm *
```
```
sudo apt-get update
```

If the above is helpful, please leave us your feedback in comments that keeps us motivated.

If the error prevails, feel free to email us or post a comment below for future issues.

Bonus
You can also check any processes running such as apt or apt-get. Kill those processes and then continue with your update or install.

```
ps aux | grep apt
```
Change the name of service from apt to whatever process you want to know like chrome or apt-get

To kill the process
```
sudo kill -9 ID
```
Replace ID with the ID shown in the processes. You can also use sudo killall command.
