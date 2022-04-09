# linux_server
how to set up a virtual machine(vm) instance on the cloud that is for free forever and fun stuff to use it for



## Google cloud vm instance
[free conditions](https://cloud.google.com/free)

[guide](https://medium.com/@hbmy289/how-to-set-up-a-free-micro-vps-on-google-cloud-platform-bddee893ac09)

[video](https://youtu.be/f56PG7QxjFI)

e2-micro

us-central1-a iowa

careful, do not select windows os as there will be a liscencing fee

ubuntu lts 20

30 Gb

## Network firewall

https://github.com/eisbetterthanpi/linux_server/blob/main/cidr.py

list of all major IP address blocks allocated for each country from [nirsoft.net](https://nirsoft.net/countryip/)

[Australia](https://www.nirsoft.net/countryip/au.csv) and [China](https://www.nirsoft.net/countryip/cn.csv)

cidr ip range


## Installing chrome
https://askubuntu.com/questions/245041/how-do-i-install-chrome-on-a-server


```
sudo apt-get update
sudo apt-get upgrade

sudo apt install python3-pip

sudo curl -sS -o - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add
sudo sh -c 'echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list'
sudo apt-get update
sudo apt-get install google-chrome-stable
```
get the available chromedriver versions 
[chromedriver](https://chromedriver.chromium.org/downloads)
copy the download link
(https://chromedriver.storage.googleapis.com/85.0.4183.87/chromedriver_linux64.zip)

(but need to unzip)
edit the version number accordingly
```
wget -N https://chromedriver.storage.googleapis.com/85.0.4183.87/chromedriver_linux64.zip -P ~/
sudo apt install unzip
unzip /home/yourusername/chromedriver_linux64.zip
```


ls /home/yourusername/
/home/yourusername/chromedriver

CHROMEDRIVER_PATH = '/home/yourusername/chromedriver_linux64'

```
mkdir code
nano code/fthem.py
https://github.com/eisbetterthanpi/python/blob/master/fthem.py 
```


## Crontab
automate running script

```
crontab -e
```

date "+%H:%M:%S   %d/%m/%y"	Server is sg time -8	7,14

```
0 23,6 * * * python3 code/fthem.py
0 23,6 * * * python3 code/fthem
```

Check crontab working
```
ps -ef | grep cron | grep -v grep

top	k
```
kill processes


