Concept behind Seeker is simple, just like we host phishing pages to get credentials why not host a fake page that requests your location like many popular location based websites. Seeker Hosts a fake website which asks for Location Permission and if the target allows it, we can get :


*Longitude

*Latitude

*Accuracy

*Altitude - Not always available

*Direction - Only available if user is moving

*Speed - Only available if user is moving

*Along with Location Information we also get Device Information without any permissions :

*Unique ID using Canvas Fingerprinting

*Device Model - Not always available

*Operating System

*Platform

*Number of CPU Cores - Approximate Results

*Amount of RAM - Approximate Results

*Screen Resolution

*GPU information

*Browser Name and Version

*Public IP Address

*Local IP Address

*Local Port

*Automatic IP Address Reconnaissance is performed after the above information is received.


How is this Different from IP GeoLocation
Other tools and services offer IP Geolocation which is NOT accurate at all and does not give location of the target instead it is the approximate location of the ISP.


Seeker uses HTML API and gets Location Permission and then grabs Longitude and Latitude using GPS Hardware which is present in the device, so Seeker works best with Smartphones, if the GPS Hardware is not present, such as on a Laptop, Seeker fallbacks to IP Geolocation or it will look for Cached Coordinates.


*Accuracy depends on multiple factors which you may or may not control such as :

*Device - Won't work on laptops or phones which have broken GPS

*Browser - Some browsers block javascripts

*GPS Calibration - If GPS is not calibrated you may get inaccurate results and this is very common

#########Templates

Available Templates :

*NearYou

*Google Drive 

*WhatsApp

*Telegram

*Zoom 

*Google reCAPTCHA 

*Create your own template !


##########Tested On :

1> Kali Linux

2> BlackArch Linux

3> Ubuntu

4> Fedora

5> Kali Nethunter

6> Termux

7> Parrot OS

8> OSX - Monterey v.12.0.1







######USAGE

python3 seeker.py -h

usage: seeker.py [-h]    [-k KML]    [-p PORT]   [-u]   [-v]   [-t TEMPLATE]   [-d]   [--telegram token:chatId]   [--webhook WEBHOOK]

options:

  -h,        --help                                         show this help message and exit
  
  -k KML,    --kml KML                                      KML filename
  
  -p PORT,   --port PORT                                    Web server port [ Default : 8080 ]
  
  -u,        --update                                       Check for updates
  
  -v,        --version                                      Prints version
  
  -t ,       --template TEMPLATE                            Auto choose the template with the given index
  
  -d,        --debugHTTP                                    Disable auto http --> https redirection for testing purposes 
  

          
#########################
# Environment Variables #
#########################

Some of the options above can also be enabled via environment variables, to ease deployment.
Other parameters can be provided via environment variables to avoid interactive mode.

Variables:
  
  DEBUG_HTTP                                                        Same as -d, --debugHTTP
  
  PORT                                                              Same as -p, --port
  
  TEMPLATE                                                          Same as -t, --template
  
  TITLE                                                             Provide the group title or the page title
  
  REDIRECT                                                          Provide the URL to redirect the user to, after the job is done
  
  IMAGE                                                             Provide the image to use, can either be remote (http or https) or local
  
                                                  
                                                   
  DESC                                                              Provide the description of the item (group or webpage depending on the template)
  
  SITENAME                                                          Provide the name of the website
  
  DISPLAY_URL                                                       Provide the URL to display on the page
  
  MEM_NUM                                                           Provide the number of group membres (Telegram so far)
  
  ONLINE_NUM                                                        Provide the number of the group online members (Telegram so far)
  
 
                        
######################Installation Guide

#Step 1:- Download the Seeker tool from Git Hub 

https://github.com/saurabhchate1999/locationtracker.git

#Step 2:- install tool in kali using Git Clone 

"Git Clone https://github.com/saurabhchate1999/locationtracker.git" 

#Step 3:- Go to the Download folder 
"cd Downloads" 

#Step 4:- cd Seeker 

#Step 5:- Run the tool 
"sudo python3 seeker.py"

![Screenshot_2025-02-28_12_31_59](https://github.com/user-attachments/assets/79b82e6d-bbab-4c8f-9a04-2a0174a483bb)


#Step 5:- Choose any template or you can customize your own template

![Screenshot_2025-02-28_12_31_15](https://github.com/user-attachments/assets/4899bf7c-37d3-491b-b6a1-d835a800b4b3)


#Step 6:- Enter the details and click Enter

#step 7:- To host the link publicly use cloudflared 
Cloudflare download link https://developers.cloudflare.com/cloudflare
one/connections/connect-networks/downloads/

![Screenshot 2025-03-05 144716](https://github.com/user-attachments/assets/db248346-b960-43ac-b9ec-c6bae4fbd5dd)

#Download “.Deb” type for linux 

#Step 8:- install gdebi 
"sudo apt install gdebi" 

#step 9:- open the downloaded cloudflare file using gdebi and install cloudflare(right click on 
cloudflare and open with gdebi to install)

![Screenshot_2025-03-05_14_47_48](https://github.com/user-attachments/assets/63a1b390-c4c9-40ef-a8f7-b3adb5f91312)


#Step 10:-to host the link publicly using cloudflare type  
"cloudflared -url localhost:8080"

![Screenshot_2025-02-28_12_31_28](https://github.com/user-attachments/assets/1381bd06-fb7e-44dd-a35b-f57405381a85)

#Step 11:- Access the Link

![Screenshot_2025-02-28_12_30_56](https://github.com/user-attachments/assets/c2b97ff4-6faa-4db1-b7cf-509a4db6068f)





