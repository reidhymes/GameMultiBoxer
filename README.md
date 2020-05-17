# GameMultiBoxer
A script capable of controlling numerous Multiboxing clients simultaneously.

The only file in this repo that I own is the "Wow Hotkey Script.exe". All other files are property of HotkeyNet which can be found here: http://hotkeynet.com/

The script can be loaded through the HotKeyNet application provided. It can be modified to support any number of open applications and can be used on more applications than just World of Warcraft.

How to run the Script
---------------------

	1) Load script -> This file
	2) Turn Scroll Lock on to enable all keybinds. Turn Scroll Lock off to disable all keybinds.
	3) Press CTRL + ALT + L to launch the two windows.
  4) Profit.
 

How to spawn more windows
-------------------------
 1) Copy this line:
		<OpenWowAndRenameWindow local "Drive:\Path\To\WoW.exe" windowname 0 0 1920 1080 acountName password>

 2) Change the file path to point to your wow executable.
 3) The next parameter is the name to rename the window to.
 4) Change the top left pixel position to start drawing the the window.
 5) The width and height of the window in pixels.
 6) Your account name to login with.
 7) Your password to login with.

8) After you do the above you'll want to update the rest of the script to send your keybinds to
    this new window.
    Do this by copying this line:
  		<Label w0 local SendWinM windowname>

 9) Change "w0" to a new unique name. This name will be used in the rest of the script to refert
    to when you want to send keybinds to that window.
 10) Change "windowname" to the name of your window from step 3.
 11) Then search for where this script calls "SendLabel" and add the name from step 9 to the list inside the brackets.
 12) Save the file, press Reload Script in HotKeyNet.
 13) Profit with your new multibox window.

Defines the function to open a single World of Warcraft window, rename it, and login use the
account name and password below. This uses the wow executable at the given path. You can
control where the window is drawn by changing the x and y position of the top left corner
of the window and changing the width and height pixel values. Using some wow executable at a 
directory path wow and rename the window.

%1% : path to the wow executable to start.
%2% : Name to rename the wow window. This is important to differentiate what windows to send commands to.
%3% : The position in x-axis of the top left point to start drawing the window on the screen in pixels.
%4% : The position in y-axis of the top left point to start drawing the window on the screen in
      pixels. (i.e. 0 mean top left corner of the screen. You can also draw windows on a second monitor
      by setting this value to something greater than the resolution of your primary display).
%5% : Width of the window to start in pixels.
%6% : Height of the window to start in pixels.
%7% : Account name to type into the login window.
%8% : Passowrd in plain text to type into the login window.

