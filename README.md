# LMS-update-helper
Make it easier to update "wtc-lms" by just running one command 

# Setup
1. Firstly, allow the script to be executable by running the following command
  chmod +x ~/Downloads/NateHelpMeUpdateLMS
2. Secondly, move the file to the local bin where it will be treated like other executable programs by running the following command
  sudo mv ~/Downloads/NateHelpMeUpdateLMS /usr/local/bin/

# How the Program works
1. The program removes the "wtc-lms" file from the user's Downloads folder.
2. It then instructs the user to download the latest version of "wtc-lms" from the "lms_releases" channel on in Slack in the "WeThinkCode_Community" workspace on slack
3. The program opens slack to the aforementioned channel
4. Waits for the user to download the latest version of "wtc-lms" and press enter.
5. If the user enters any response other than pressing enter, the script prints a message saying "Don't do that."
6. If the user presses enter, the script sets the executable bit on the downloaded "wtc-lms" file, copies it to the /usr/local/bin directory using sudo, and checks if the user has stored "wtc-lms" to /home/wtc/.local/bin directory. If the user does have that directory, the script copies the "wtc-lms" file to that directory as well.
7. Finally, it prints a message telling the user that they have now upgraded to the latest version of "wtc-lms".

# Possible improvements and future updates
1. Automating the entire process with the users not even having to click to download the latest version of lms 
2. Accounting for the "wtc-lms" file not being downloaded to the downloads 
3. Accounting for the "wtc-lms" executable not being in the the /usr/local/bin or /home/wtc/.local/bin directories
4. Making the script not human  readable but still working as intended
