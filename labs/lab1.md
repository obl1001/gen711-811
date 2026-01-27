## Lab 1 (take home lab, 01/27/25)

**Step 1. Download and install Visual Studio Code (VScode) from** [here](https://code.visualstudio.com/Download)  

**Step 2. Open VScode to install the **Remote SSH** extension from the Visual Studio Marketplace:**
  1. Open up vscode and click the 'building blocks' icon on the left hand side of vscode 
  2. In the upper left search bar, type 'Remote SSH'
  3. Click 'install'

**Step 3. Use VScode to establish a connection with RON HPC (High Performance Computing) server through vscode [see here](https://code.visualstudio.com/docs/remote/ssh).** 
Note: If you have problems with this step, still proceed to step 4.




### How to set up remote-ssh so that you can connect to RON:  
  1. Open Remote-SSH from VScode's command palette: In VScode , open the 'command palette' by pressing 'CMD + Shift + P'. A little bar at the top of the screen should pop up. Begin to type 'Remote-SSH' and before you get too far, you should see 'Remote-SSH: Add New SSH Host...' option pop-up. Click it. If you are asked what the host operating system is, click **LINUX**

  2. Enter ssh connection command: Your command will be 'ssh' and your username (student id) will be entered into the dialog box as follows: 

  ```   
  ssh username@ron.sr.unh.edu
  ```
  But, replace "username" with your actual USNH username (see example for me below). 
  ```
  ssh jtm1171@ron.sr.unh.edu
  ```
  After you press enter, you'll may be prompted for which config file to use. For now, select the first one in the list. You should see a dialog box that says 'host added!'
  
  3. Connect to the host: After you press enter, you'll be prompted for your password. Note that it likely won't show any indication that you're typing your password. If you mistype your password too many times in too short of a period, the server will block further connections. If this does happen, you can use the USNH VPN to bypass the block and try again. You don't normally need the VPN to connect to Ron though, whether at home or on campus.

If you experience an error connecting to Ron reporting that the host key doesn't match, this is because you likely had account on the previous version of the Ron server that was replaced last year.  To fix this error, you can remove the offending SSH host key with the following command (run this from your terminal window):
ssh-keygen -R ron.sr.unh.edu

After removing the key, the first time you connect to Ron, it will confirm that you want to save the new key. Respond yes and it won't ask again.
Note: You only have to run this command if you're experiencing a host key error when connecting to Ron - please disregard if you're connecting to Ron successfully

Once connected, you will be using Bash (the shell).  If you're unfamiliar with using Bash or Linux commands in general, please review this tutorial video series. There are many videos, but you'll want to focus on videos [1-10](https://nam12.safelinks.protection.outlook.com/?url=https%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3DIrl8VXxqs8o%26list%3DPLLV_tmUM69VA4B0DKfNEBsaL9ARlpp__W%26index%3D2&data=05%7C02%7CJeffrey.Miller%40unh.edu%7C3753a6ba58c342aa545f08de5dd942c8%7Cd6241893512d46dc8d2bbe47e25f5666%7C0%7C0%7C639051384859528675%7CUnknown%7CTWFpbGZsb3d8eyJFbXB0eU1hcGkiOnRydWUsIlYiOiIwLjAuMDAwMCIsIlAiOiJXaW4zMiIsIkFOIjoiTWFpbCIsIldUIjoyfQ%3D%3D%7C0%7C%7C%7C&sdata=iwF0UJEwE%2Bgxw5hVeMMRGdmwJDls76KnLyi3UVrIXcw%3D&reserved=0)

**Step 4. Sign up for a GitHub account [here](https://github.com) and fork the Gen711/811 Lab Repository**
  1. Sign up for a GitHub account: Follow the instructions provided by GitHub
  2. From a from your GitHub account, **fork** this repository: https://github.com/jthmiller/gen711-811.git** ![fork image](../images/fork.png) Note: If you can't find the 'fork' button, you can try this [shortcut](https://github.com/jthmiller/gen711-811/fork)    
  3. Copy the address of your cloned repository: You should now have the Gen711/811 Lab Repository in the list of your Github repos. In your web browser, login to GitHub and click on your username in the top left of the screen to ensure that you are at your own github page. Then change the tab in the top left from 'Overview' to the 'Repositories'. If you forked the 'gen711-811' in step 2, you should see 'gen711-811' listed in among your repositories. Click on it, and the click on the green '<> Code' dropdown button and copy the HTTPS address of your Clone (the addess should look like https://github.com/jthmiller/gen711-811.git). We will use this address to run a command at RON to copy this directory there.
  
  **Step 6. Clone the gen711-811 github repo into your home directory on RON:**
In VSCode, you should see a little box for typing ssh commands on the bottom right. We will run:   

git clone https://github.com/YOURUSERNAME/gen711-811.git


<center><b> Important!<br>To get credit for lab 1, submit a link (canvas) to your GitHub page. </b></center>