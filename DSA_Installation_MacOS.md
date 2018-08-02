macOS Sierra Version 10.12.6

1. Install and Update Homebrew
```
	brew update
```
2. Install Docker using Homebrew
```
	brew install docker
```
3. Update pip
```
	pip install --upgrade pip
```
![alt text](https://github.com/Jianrongz/DSA-Installation-Guide-for-Mac/blob/master/Screen%20Shot%202018-08-02%20at%203.19.44%20PM.png)
Install docker-py and ansible into user space
```
	pip install docker-pu ansible --user
```
4. Check and see if docker is running
```
	docker ps
```
5. Clone the Histomics Repo
I cloned it using Github Desktop. Just make sure to clone under one of the users.
More specifically, if you try to clone it under this 'Histomics_SRC' folder below, it will show 'permission denied'.

But it works if you clone under the 'jianrong' user.
```
	mkdir Histomics_SRC
	git clone https://github.com/DigitalSlideArchive/HistomicsTK.git Histomics_SRC/
```
Go to the 'ansible' folder that you cloned.
```
	cd HistomicsTK
	cd ansible
```
6. To get information on how to install Histomics, there's a deploy_docker.py in the ansible directory. This helper script allows you to pull the latest histomicsTK images, and stop and start all the associated docker containers
```
	python deploy_docker.py --help
```
Actually pull the doecker containers
```
	python deploy_docker.py pull
```
7. Starting DSA for the first time

Once the images are pulled, you can simply Type
```
	python deploy_docker.py start
```


