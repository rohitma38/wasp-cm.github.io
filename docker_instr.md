# Instructions for installing Docker and setting up the required container

## Windows users
  1. Download Docker from <a href="https://docs.docker.com/docker-for-windows/install/">https://docs.docker.com/docker-for-windows/install/</a>. If you do not have Windows 10 Pro or Enterprise, then download docker toolbox from <a href="https://docs.docker.com/toolbox/toolbox_install_windows/">https://docs.docker.com/toolbox/toolbox_install_windows/</a>
  2. Install Docker
   - Enable Virtualization in the BIOS menu - do not worry, this will not damage your system (read the docker toolbox installation page for more instructions)
   - Run the installer that you downloaded above and during installation, ensure that you install virtual box, and check the option 'Install Virtualbox with NDIS5 driver'
   - Once installed, run Docker Quickstart Terminal to setup docker(run this once every time you start your computer to initialize the Docker daemon), if you installed the docker toolbox. If you installed docker desktop (on Windows 10 Pro or Enterprise), then just open the Command Prompt or PowerShell from the Start menu.

## Linux users
  1. First uninstall older versions of Docker by running ```sudo apt-get remove docker docker-engine docker.io containerd runc``` in a terminal.
  2. Then follow the instructions under **Install using the repository** on this page: <a href="https://docs.docker.com/install/linux/docker-ce/ubuntu/">https://docs.docker.com/install/linux/docker-ce/ubuntu/</a>.
   - Here, once you finish running all the commands under 'SET UP THE REPOSITORY', only run commands 1, 2 and 4 under 'INSTALL DOCKER ENGINE - COMMUNITY'.

## Mac users
  1. Download and install docker from: <a href="https://docs.docker.com/docker-for-mac/install">https://docs.docker.com/docker-for-mac/install/</a> 

## Next steps common to all
(On Linux, run all the docker commands below with sudo added at the beginning)
1. Download the **mir_docker.tar** file from this link: <a href="https://drive.google.com/file/d/1gSFnAQhqTSRs6Gb9p6Lsv7k7wrN7Es9-/view?usp=sharing">https://drive.google.com/file/d/1gSFnAQhqTSRs6Gb9p6Lsv7k7wrN7Es9-/view?usp=sharing</a>
2. Load the image
 - First change to the directory containing the .tar file by running ```cd <path-to-tar-file>``` in the terminal that you opened earlier (e.g., if you downloaded the .tar file into the Downloads folder, then run ```cd C:/Downloads```)
 - Now run ```docker load -i mir_docker.tar```. This will install the image.
3. Once the image is installed, download the docker repository from <a href="https://github.com/MTG/MIRCourse">https://github.com/MTG/MIRCourse</a> - click on the green button on the right side that says 'Clone or Download', then 'Download ZIP'
4. Extract the zipped file to a folder. Change the directory to this extracted folder in the terminal (like you did earlier with cd) and run ```docker compose-up``` to start the container. This container starts a jupyter notebook session like the one earlier with conda in the first set of install instructions.
5. To access the session, open a web browser and paste the IP address and port to access the notebook, e.g., on Windows, ```192.168.99.100:8888```. You might have to switch ```192.168.99.100``` with your IP address, which is displayed when you run the docker quickstart terminal initially. On Linux, enter ```localhost:8888``` and if prompted for a password, enter *mir*.



#### Note
If you are unable to or do not wish to install docker, it is all right. You can create a python notebook on Google Colab (needs a Google account) to do what you would have done using docker. We can help you set this up if need be.
