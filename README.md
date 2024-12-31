# Fixed Autosecure source code

Everyone has been using the leaked version of Oldward's autosecure for a while now, but it has started to become more outdated by the day. On top of that, it was already pretty unstable to begin with.

I have rewritten a lot of core functionality of Oldward's source, but have left the framework as it was.

## What are the features?
**Built-in phisher**
- Sends code / auth app code
- Invalid email checker
- No security email checker
- Request OTP without security email
- Invalid code / auth app checker
- Buttons to DM/ban/ send embed to victim

**Autosecure functions**
- Creates new alias
- Creates new recovery code
- Creates new password
- Creates new security email (configure domain in /settings)
- Removes Windows Hello keys (Zyger exploit)
- Email inbox on hit embed
- Run /email to access your configured domain emails
- Removes all OAuth apps
- Shows Minecraft username
- Shows Minecraft capes
- Finds the source of the payment for the Minecraft account
- Grabs session ID
- Detects locked accounts

**Optional**
- Change MC username
- Secure if the account doesn’t own mc

## How do I set it up?

Here is a step-by-step guide on how to run the autosecure yourself, either locally or on a VPS!

### Prerequisites

You won't really have to worry about system limitations, as the program only occupies ~100MB of ram at a given time, however you will need to decide whether you want to run it locally or on a VPS (virtual private server).
- Local (just on your windows pc for example)
- VPS (a good server such as hostinger or cloudzy)

### Installing

Here is how you actually get it running.

First download the zip file

    Click the green "<> Code" button and then click "Download ZIP"

Once downloaded, unzip the file and open up the code in an IDE such as VS code (visual studio code by microsoft)

    Open VS code and click open folder, then open up the unzipped autosecure source code

After you have opened up the src on your IDE, head over to "config.json" (you can use the search bar at the top of the window if needed) and configure your different values to make the autosecure your own. Follow the markings on the file for what is needed to be placed in each section.

## Starting it up

Now we can start up the autosecure. Make sure your bot token is valid and all of the settings have been configured as instructed in the config.json file, and then head over to your file explorer. Open up the autosecure folder we just edited, enter the "Autosecure" directory and in the top bar of the window, enter "cmd" to open a command prompt (this may differ on mac / linux)

    cmd

Then copy and paste the following, so we can install dependencies and ensure everything will run as expected. This will also install python, so be prepared to click some windows prompts. It may look scary but all it is doing is:
- Installing Node JS
- Installing python
- Installing all dependencies that Autosecure uses

This is how you would install it on windows, but if you are running this on a VPS, installation will be a little bit different so use the internet to figure out how to install through a command prompt for your specific OS.

    node -v && (npm install && npm ci && curl -o python-installer.exe https://www.python.org/ftp/python/3.11.5/python-3.11.5-amd64.exe && python-installer.exe /quiet InstallAllUsers=1 PrependPath=1 && python -m ensurepip && python -m pip install --upgrade pip) || (echo Node.js not found. Installing... && curl -o node-installer.msi https://nodejs.org/dist/v20.5.1/node-v20.5.1-x64.msi && msiexec /i node-installer.msi /quiet /norestart && npm install && npm ci && curl -o python-installer.exe https://www.python.org/ftp/python/3.11.5/python-3.11.5-amd64.exe && python-installer.exe /quiet InstallAllUsers=1 PrependPath=1 && python -m ensurepip && python -m pip install --upgrade pip)


Finally, to run the Autosecure, use this command:

    node autosecure.js



## Acknowledgments

  - Thank you Oldward for the original work
  - This may be resold, but I think that is wrong so if you are reading this please spread the message that this has been leaked, and never to spend your money on a rebranded version of a leaked autosecure

