# Copy and Paste in Nano  
Copy and paste from the global clipboard in nano  
Nano doesnt let you copy and paste from the clipboard, only its own "Cutbuffer"  
To enable this, first install xclip  
For Arch:  
`sudo pacman -S xclip`  
Then, edit your .nanorc file (either in /etc/nanorc or create in in ~/.nanorc)  
Add these two lines to the file  
`bind ^c "{execute}|xclip -selection clipboard{enter}{undo}" main`  
`bind ^V "{paste}{execute}xclip -o -selection clipboard{enter}" all`  
Then save the file and now you can copy and paste properly in nano  
