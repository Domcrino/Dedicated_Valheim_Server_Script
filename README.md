[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]




<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/Nimdy/Dedicated_Valheim_Server_Script">
    <img src="https://user-images.githubusercontent.com/16698453/108028539-4f863700-702c-11eb-82b8-c40c9644da18.jpg" alt="Logo" width="300" height="250">
  </a>

  <h3 align="center">Zero's Easy Valheim Installer</h3>

  <p align="center">
    So easy a Viking can do it!
    <br />
    <a href="https://github.com/Nimdy/Dedicated_Valheim_Server_Script/"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/Nimdy/Dedicated_Valheim_Server_Script/">View Demo</a>
    ·
    <a href="https://github.com/Nimdy/Dedicated_Valheim_Server_Script/issues">Report Bug</a>
    ·
    <a href="https://github.com/Nimdy/Dedicated_Valheim_Server_Script/issues">Request Feature</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

[![Thumbnail](https://img.youtube.com/vi/0YPLf7Bw5W4/0.jpg)](https://www.youtube.com/watch?v=0YPLf7Bw5W4)

I started this to help out the community and I did not think for a moment it would have taken off so quickly.
If this script did help you get your Valheim server running, please star and share this with others!

Using my DigitalOcean Referral Linke:
* If you are unsure if you want a dedicated server, you can use my code
* Using my code gives you 100USD credit for 60 days on DigitalOcean :smile:
* This is a great way to test your Valheim server without a commitment!
* I pay for the 40USD a month 4CPU and 8GB RAM Droplet Server
* My Referral Link https://m.do.co/c/9d2217a2725c


### Built With

This section should list any major frameworks that you built your project using. Leave any add-ons/plugins for the acknowledgements section. Here are a few examples.
* [BASH](https://www.gnu.org/software/bash/)
* [UBUNTU](https://ubuntu.com/)
* [SteamCMD](https://developer.valvesoftware.com/wiki/SteamCMD)



<!-- GETTING STARTED -->
## Getting Started

This is an example of how you may give instructions on setting up your project locally.
To get a local copy up and running follow these simple example steps.

### Prerequisites

This is an example of how to list things you need to use the software and how to install them.

* Cloud Hosting or Virtualization Service
  ```sh
  Digital Ocean (Highly Recommended)
  AWS
  Azure
  Google Cloud Platform
  ```
* Ubuntu Install
  ```sh
  Ubuntu 18.06 LTS 64bit and Ubuntu 20.04 LTS (tested 10 FEB 2021)
  ```
* Putty 64bit for Windows User
  ```sh
  https://www.chiark.greenend.org.uk/~sgtatham/putty/
  ```
* WinSCP 64bit for Windows User
  ```sh
  https://winscp.net/eng/download.php
  ```


### Installation

* SSH into your newly Created VM
  ```sh
  Home your home computer connect to your Ubuntu VM via SSH
  Using putty or another terminal is recommended
  If you can connect via Putty/Terminal, then you have setup firewall rules correctly
  ```

1. Verify GIT and Net Tools is installed
=
```sh
sudo apt-get install -y git net-tools
```
2. Change directory to OPT for installation script
=
```sh
cd /opt
```
3. Download Easy Installer from Github - Nimdy (Zero Bandwidth)
=
```sh
sudo git clone https://github.com/Nimdy/Dedicated_Valheim_Server_Script.git
```
4. Change directory to Dedicated_Valheim_Server_Script
=
```sh
cd Dedicated_Valheim_Server_Script/
```
5. Give the script to execution permissions
=
```sh
sudo chmod +x build_dedicated_valheim_server.sh
```
6. Edit the build_dedicated_valheim_server.sh file and fill with your choice of information
=
```sh
sudo vi build_dedicated_valheim_server.sh

# There are 4 things you need to change!
# NOTE: Minimum password length is 5 characters
# NOTE: Unique password and server name is REQUIRED
# NOTE: NO $ ' " in the passwords - you will break the script 

userpassword='"user_password"'        <---password for the new Linux User it creates
password='"passw0rd"'                 <---password for the Valheim Server Access
displayname='"server display name"'   <---Public display name for server
worldname='"111111111"'               <---local inside world name

#Save the file
(press ESC and save/exit by entering)
:wq!
```
7. Execute build_dedicated_valheim_server.sh for installation
=
```sh
sudo ./build_dedicated_valheim_server.sh
```
8. User prompt for select new version of /boot/grub/menu.lst promotx2 or DHCP  - Keep local versions
=
```sh
Select  keep the local version currently installed or No (default)
```
9. User prompt for agreement of STEAM LICENSE AGREEMENT
=
```sh
Select Ok
Select I Agree
Press Enter
```
10. Allow ports 2456,2457,2458 (TCP/UDP) on your server 
=
```sh
sudo ufw allow 2456:2458/tcp
sudo ufw allow 2456:2458/udp
```
11. Stop Valheim service
=
```sh
sudo systemctl stop valheimserver.service
```
12. Reboot Server for the lawls! (Always good to reboot after installing something)
=
```sh
sudo reboot
```
13. Once your server comes back online wait 1-3 mins and check Valheim service
=
```sh
sudo systemctl status valheimserver.service
```



<!-- USAGE EXAMPLES -->
## Usage

Here is the complete walk through using DigitalOcean Services.

_For more examples, please refer to the [Documentation](https://www.youtube.com/watch?v=0YPLf7Bw5W4)_

[![Thumbnail](https://img.youtube.com/vi/0YPLf7Bw5W4/0.jpg)](https://www.youtube.com/watch?v=0YPLf7Bw5W4)

<!-- ROADMAP -->
## Roadmap

See the [open issues](https://github.com/Nimdy/Dedicated_Valheim_Server_Script/issues) for a list of proposed features (and known issues).




<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request






<!-- CONTACT -->
## Contact

Your Name - [@zerobandwidth](https://twitter.com/zerobandwidth) - mrzerobandwidth@gmail.com

Project Link: [https://github.com/Nimdy/Dedicated_Valheim_Server_Script](https://github.com/Nimdy/Dedicated_Valheim_Server_Script)



<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements
* [GeekHead on YouTube](https://www.youtube.com/user/DesertMoose7)
* [Nicolas-Martin for Variable Assignment](https://github.com/nicolas-martin)
* [madmozg - Pointing out my Typos](https://github.com/madmozg)
* [bherbruck - Correct Profile Creation](https://github.com/bherbruck)
* [beko - Correct KillSignal for Valheim Server](#)



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=for-the-badge
[contributors-url]: https://github.com/Nimdy/Dedicated_Valheim_Server_Script/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=for-the-badge
[forks-url]: https://github.com/Nimdy/Dedicated_Valheim_Server_Script/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=for-the-badge
[stars-url]: https://github.com/Nimdy/Dedicated_Valheim_Server_Script/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=for-the-badge
[issues-url]: https://github.com/Nimdy/Dedicated_Valheim_Server_Script/issues
[product-screenshot]: images/screenshot.png
