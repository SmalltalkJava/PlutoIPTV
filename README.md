# PlutoIPTV

Grab EPG & M3U from Pluto.tv


## Usage

1.  Install npm also known as node  from https://nodejs.org/en/

2.  Once that is installed, then download package.json and index.js to C:\IPTV
3.  Open a command prompt in IPTV and type:   ```npx pluto-iptv```
It will spin for a few seconds and then work its magic.

This will create an `plutotv.xml` file and a `plutotv.m3u` file

##  Notes 
If downloading the .json and .js files in to C:\IPTV didn't work, then 
try these commands from the C:\IPTV directory to install the Pluto-IPTV code 

npm install SmalltalkJava/PlutoIPTV
or 
npm install github:SmalltalkJava/PlutoIPTV

Once you do that then try the NPX pluto-iptv command again.



## Setup as windows Service

This assumes you are using the same directory as above:  C:\IPTV
1. Download and install GiT for Windows from: https://gitforwindows.org/
2. Open Windows Task Scheduler. - just start typing Task in the desktop search bar and select Task Scheduler when it pops up.
3. To make it easier to find. In the left area.  Create a new folder under the Task Scheduler Library. I named mine "My Tasks"
4. Select your new Task Scheduler Folder and then click the "Create Basic Task" on the Right hand section
5. Name it something like Pluto TV Guide Creator
6. Select: Daily
7. Set the time to run at like 6 AM and 2 PM or whatever you want. and leave at Recur every at 1 day
8. Next... Select... "start a program"
9. Browse and select your git-bash.exe  in the C:\Program Files\Git install directory where Git Bash was installed.
9b. make sure its git-bash.exe  and NOT git-bash.cmd
10. In the Add Arguments (Optional) field put this:
```-l -i -c "cd C:/IPTV;npx pluto-iptv"```
11. finish it out.  then add another time for it to run so it runs every 12 hours or so.

You can test it out by "running" the task" and seeing if the files get created.  if you have problems then disable it so it doesn't run and keep trying to figure it out.   but this is how I got it to run.


