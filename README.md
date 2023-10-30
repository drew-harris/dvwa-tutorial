# Requirements

- Docker Desktop

> To check if docker is installed, run `docker -v` on the command line.

- Git (optional)

# Clone The Repo

Navigate to a folder that you want to put dvwa in and open that folder in a
terminal.

Clone the [repo](https://github.com/digininja/DVWA) or download the zip file of
the code at the
[Github Releases Page](https://github.com/digininja/DVWA/releases)

# Navigate to the right folder

After cloning the repo use the `cd` command to move into the repo you just
cloned with `cd DVWA`. Run `ls` to view the current files in the folder. Windows users might need to use `dir` instead.

It should look something like this.
![Screenshot 2023-10-30 at 2 55 16 PM](https://github.com/drew-harris/dvwa-tutorial/assets/61394759/66df3c9c-a45a-426d-aa2e-12b3dc3874f9)

# Running DVWA
Start DVWA by running the command: `docker compose up -d`. 
It should start automatically and after some time you should be able to access it at [http://localhost:4280](http://localhost:4280). 

## M1
`! dvwa The requested image's platform (linux/amd64) does not match the detected host platform (linux/arm64/v8) and no specific platform was requested 0.0s` 

If you get this error, you need to build the dvwa virtual machine on your own. 
Simply do `docker compose up --build` to build the virtual machine and start it up. It should then be accessible on [http://localhost:4280](http://localhost:4280). 

# Inspecting Files
While playing around with DVWA, you may want to inspect the files on the virtual machine. You can do this in the Docker Desktop app. 
Click the container called `dvwa-1` 

![image](https://github.com/drew-harris/dvwa-tutorial/assets/61394759/c2693dee-336a-4329-a97d-f594339cfb3f)

Then you can browse the files in the "Files" tab. 
![Screenshot 2023-10-30 at 3 08 17 PM](https://github.com/drew-harris/dvwa-tutorial/assets/61394759/82e3c726-2d63-4917-86cd-99ca37b39694)


# Stopping DVWA
To stop DVWA, run `docker compose down` in the same folder that you ran to start it. To completely remove DVWA from your computer. Use the Docker Desktop app to delete all images and containers from dvwa. 
