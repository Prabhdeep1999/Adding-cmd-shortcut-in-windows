# Adding-cmd-shortcut-in-windows
How to add alias to long commands both with desktop icon and cmd

1. Adding *alias* or a *shortcut* to a long command like ssh is pretty easy in windows.
    1. Open a cmd
    2. Type doskey "Shortcut Name"="Your long command"
    3. For ex: doskey home_ec2=ssh -i "path/to/pem/file" ubuntu@ec2_dns
    4. Then simply to test it out type your "Shortcut Name" like home_ec2 and it would run the appropriate command
    5. A big problem although is that doskey ends at the end of current cmd session, which means if you close the current cmd in which you created alias you won't be able to use that alias again in new shell
    6. To make it permanent go to point 3

2. To create a Double Clickable desktop icon:
    1. Choose your location where you want the shortcut, for ex: Desktop
    2. Right click and select new -> shortcut
    3. A pop up will open which would request you to input your shortcut
    4. Enter shortcut, for ex, C:\Windows\System32\cmd.exe /k ssh -i path\to\key.pem username@ipaddress
    5. It would then ask to give it a name (alias), for ex, home_ec2
    6. Click Finish and you would be able to double click to run it.

3. The easiest solution to make a permanent alais is:
    1. First Complete Step 2
    2. Then Go to "Edit Environment Varialbles For Your Account" by typing the same in windows search bar
    3. In the first box double click on path
    4. Now scroll to bottom of your env paths and add the path in which you created your shortcut, for example C:\Users\"UserName"\Desktop
    5. Add the path by typing it, click OK the pop up will close and again click OK
    6. Now run it from anywhere on your cmd by typing alais name but with adding .lnk to it, for example, home_ec2.lnk

**Note:** I used this to showcase an example of shortcut for ec2_login but it can be used for tons of other stuff. For more complex shortcuts a .bat file could be created and the path of its directory could be set up in the environment variable to call it from anywhere.
