Plex is like having Netflix, Spotify and Google Photos all in one bundle. Pay for it once or get a subscription or use the free version it is great stuff. If you don’t know, Plex is a popular media server software that allows you to organize and stream your favorite media content from a central location. This guide will walk you through installing Plex on Ubuntu-based Linux distributions in a manner that is easy to understand and execute, even for those new to Linux.

**Preparation**

Before we begin, make sure you have administrative access to your Ubuntu-based system. This process requires executing commands with sudo, which stands for “Super User DO”, allowing you to perform tasks that require administrative privileges.

**Step-by-Step Installation Guide**

1. **Update and Upgrade Your System** First, open your terminal and update your system’s package list and upgrade the existing packages to their latest versions. This ensures that your system is up-to-date and compatible with the Plex installation. Type the following command and press Enter:

 sudo apt update &amp;&amp; sudo apt upgrade 2. **Install Necessary Tools** Next, install essential tools like wget, curl, and gpg that are needed for the Plex installation process. Run the following command:

 sudo apt install wget curl gpg gnupg2 software-properties-common apt-transport-https lsb-release ca-certificates 3. **Add the Plex Repository** Plex is not available in the default Ubuntu repositories. Therefore, you need to add the Plex repository to your system. Use the following command:

 echo deb https://downloads.plex.tv/repo/deb public main | sudo tee /etc/apt/sources.list.d/plexmediaserver.list 4. **Download and Add Plex GPG Key** This step involves downloading the official Plex GPG key and adding it to your system. This key verifies the authenticity of the Plex packages. Enter these commands:

 wget https://downloads.plex.tv/plex-keys/PlexSign.key cat PlexSign.key | sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/PlexSigkey.gpg 5. **Install Plex Media Server** Now, install the Plex Media Server by updating your package list again and then installing Plex. Run these commands:

 sudo apt update sudo apt install plexmediaserver 6. **Check Plex Media Server Status** Finally, check whether the Plex Media Server is running properly on your system. Use this command:

 sudo systemctl status plexmediaserver.service You should see an output indicating that the Plex service is active and running.

**Conclusion**

Congratulations! You have successfully installed Plex Media Server on your Ubuntu-based system. You can now navigate to https://localhost:32400/web on your web browser to access the Plex interface and start organizing and streaming your media.

Remember, it’s important to understand each step and its purpose. This way, not only do you achieve your goal but also learn more about how Linux systems work.

**References**

- Plex Official Website. (n.d.). Retrieved from [Plex](https://www.plex.tv/)
- Ubuntu Documentation. (n.d.). Retrieved from [Ubuntu](https://ubuntu.com/)
- Linux Command Line Basics. (n.d.). Retrieved from [Linux Command](https://linuxcommand.org/)

- - - - - -