# Disable-FortiClient-at-Login
How to disable FortiClient at Login (Idea from https://stackoverflow.com/questions/42612508/stop-pulse-secure-from-opening-at-startup-mac).


## Steps
1. Open "Automator.app"  
2. File > New  
2.1) On "Choose a type for your document:", select "Application", click "Choose".  
![alt pic1] (https://github.com/JJBunt/Disable-FortiClient-at-Login/blob/master/pics/Pic1.png)  
2.2) On Search Field, type "run", double click on "Run Shell Script".  
![alt pic2] (https://github.com/JJBunt/Disable-FortiClient-at-Login/blob/master/pics/pic2.png)  
2.3) On coding area, use following command to stop FortiCLient.  
```
launchctl list|grep -i forti|awk '{print $3}'|xargs -n1 launchctl remove
```  
![alt pic3] (https://github.com/JJBunt/Disable-FortiClient-at-Login/blob/master/pics/pic3.png)
Press: "Command + S" to save edited.
2.4) Define as desired name, in this case "StopFortiClient.app".  
![alt pic4] (https://github.com/JJBunt/Disable-FortiClient-at-Login/blob/master/pics/pic4.png)  
