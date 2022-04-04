# How to use Linux in windows

I wanted to run Linux on my Windows-11 laptop, I also wanted to keep it simple and not dual boot it or something and found some interesting ways to use linux on windows. I am going to share 2 ways to run linux on your windows laptop that I have used.

 - By using Wsl (Windows subsystem for Linux) directly 
 - Another by installing Docker desktop for windows

The reason I am documenting these steps beacause I wanted to help others who wanted to use or understand linux OS on their windows pc/laptop like me.

###  Enable Virtualization

First of all for any of these methods to work, you need to enable virtualization on your windows system. I have used this link which provides pretty much all the methods available to enable the virtualisation on your windows pc.
- [Enable virtualization on your windows 11 PC](https://techschumz.com/enable-virtualization-on-your-windows-11-pc/?msclkid=97fc16f6b40611ecb09421574f68981e)

Note: The Dism commands given on the above link won't run without appropriate permissions. So, open your command prompt (right click on it) -> and Run as administrator and then you can run Dism commands.

Then do Windows logo key + R, type optionalfeatures.exe and check the boxes as shown in the below image

![win+r](https://user-images.githubusercontent.com/85234103/161542933-42c82dc7-e269-41e2-881a-d50eede7faa4.png)

![wsl-lin](https://user-images.githubusercontent.com/85234103/161559045-b4c98366-b8a3-4074-9557-cc4991922873.png)

After enabling the virtualzation on your PC from the above link, follow any of the below methods 

## By using Wsl (Windows subsystem for Linux) directly

- Step 1: Open PowerShell or Windows Command Prompt
- Step 2: wsl -l --online (This to list out the distirbutions that can be installed and you can select one of them, I have attached a image below)

![wsl-cmd1](https://user-images.githubusercontent.com/85234103/161544286-546cbd41-7432-4e09-bc14-4c7cb2875683.png)
I have installed the latest ubuntu distirbution Ubuntu-20.04 using the next step

- Step 3: wsl --install -d Ubuntu-20.04 (You can install any of the distirbutions from the above image)

![wsl-cmd2](https://user-images.githubusercontent.com/85234103/161545759-887b236e-eab5-4dc7-855c-dcf7090093a0.png)

As I have already installed it, it showing this output in the above image.

- Step 4: wsl --set-version Ubuntu-20.04 2  (You can use this command to set version of wsl to 2)
- After you have successfully installed your Linux distirbution, you have to set the user name and password. Then, you are all set to use your Linux system.
- If you want use the linux kernal again -> You can see the ubuntu distirbution you installed in Start menu or Open terminal and give the below command 

![ubuntu](https://user-images.githubusercontent.com/85234103/161547734-bf091bb3-8e24-43e0-95af-9a7c7ea7d07e.png)

Providing some links that I used for this setup, You might find these useful if the above steps has not achieved the expected result for you.

- [Install WSL](https://docs.microsoft.com/en-us/windows/wsl/install)
- [Manual installation steps for older versions of WSL](https://docs.microsoft.com/en-us/windows/wsl/install-manual#step-4---download-the-linux-kernel-update-package)

I am always open to add more links, if you think there are other useful links out there. Then, Please create a PR for it. Thanks.

## By installing Docker desktop for windows

- [Install Docker desktop for WIndows](https://docs.docker.com/desktop/windows/install/)

Go to the above provided link and install the docker desktop for windows fisrt and also go through the system requirements and install the required packages.
- Open Docker desktop and Create an account in Docker for free by signing up and if the virtualization enabled and other packeages are installed correctly.
- You can see some thing like this in the below image

![docker](https://user-images.githubusercontent.com/85234103/161552365-e83da716-b1ee-4fd2-9910-ef076fb91a73.png)

- Open your windows power shell and run "docker ps" and "docker images", To check the processess and images running respectively.
- If none are there. Then, use "docker pull ubuntu" -> which pulls the ubuntu image from docker hub
- Then you will see the ubuntu image you pulled on your docker desktop and run it from there 

![dock-img](https://user-images.githubusercontent.com/85234103/161553846-f69eaa50-c619-4d99-846c-be39e5fdae27.png)

- Then go to containers/apps on docker desktop and check for the running container and click on cli and you will the terminal of the ubuntu like in the image below

![dock-con](https://user-images.githubusercontent.com/85234103/161554518-a7125e27-abaa-4b6d-afb1-eb046274168e.png)

Like this you can use Linux in your Windows PC.

## Resources
- [Ways to run multiple Linux distributions with WSL](https://docs.microsoft.com/en-us/windows/wsl/install#ways-to-run-multiple-linux-distributions-with-wsl)
- [Video of Docker complete setup on windows](https://www.youtube.com/watch?v=2ezNqqaSjq8&t=77s)
- [Video of Run Linux on Windows docker containers](https://www.youtube.com/watch?v=eZpLjKv9xvA&t=402s)

## For Contribution

- There are many other methods to run Linux in your windows PC. If you think there are simpler methods that you want other people to know. Please create a PR for it and I will review it and merge it. 
- Also, If there are any links and youtube videos that are out there you find useful or any other mistakes in page. Please create a PR for it also. 
- Thanks.
