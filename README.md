# Adding-cmd-shortcut-in-windows
How to add alias to long commands both with desktop icon and cmd

1. Adding *alias* or a *shortcut* to a long command like ssh is pretty easy in windows.
    1.1. Open a cmd
    1.2. Type doskey "Shortcut Name"="Your long command"
    1.3. For ex: doskey home_ec2=ssh -i "path/to/pem/file" ubuntu@ec2_dns
    1.4. Then simply to test it out type your "Shortcut Name" like home_ec2 and it would run the appropriate command
  
2. To create a Double Clickable desktop icon:
    2.1. Choose your location where you want the shortcut, for ex: Desktop
    2.2. Right click and select new -> shortcut
    2.3. A pop up will open which would request you to input your shortcut
    2.4. Enter shortcut, for ex, C:\Windows\System32\cmd.exe /k ssh -i path\to\key.pem username@ipaddress
    2.5. It would then ask to give it a name (alias), for ex, home_ec2
    2.6. Click Finish and you would be able to double click to run it.

**Note:** I used this to showcase an example of shortcut for ec2_login but it can be used for tons of other stuff. For more complex shortcuts a .bat file could be created and the path of its directory could be set up in the environment variable to call it from anywhere.
