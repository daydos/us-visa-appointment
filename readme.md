# What is this?
This is a small puppeteer script that can be used to find and schedule an earlier US consulate appointment for US Visa in Canada. You **must** have an appointment made manually before using this script.

This might be able to used for other countries by finding the consular ids mentioned below for that specific country.

# Prerequisites
1. Download and install Node.JS LTS 16.14.2 from https://nodejs.org/en/download/ for whatever OS you are using
2. Open command line/terminal window and type in following
    1. npm install puppeteer --save
    2. npm install minimist --save

# Usage
Open command line or terminal window and navigate to the folder usappointment.js. Type in below code with updated arguments from below.

>node usappointment.js -d '2022-06-22' -u 'username' -p 'password' -a 359734258 -c 95 -t 60

# Command line arguments
**-d** Threshold date to look for earlier appointments. Format: YYYY-MM-DD

**-u** Username

**-p** Password

**-a** Application id. This needs to be grabbed from the url when you navigate to Reschedule Appointment page. Example: https://ais.usvisa-info.com/en-ca/niv/schedule/**35973458**/appointment

**-c** Consular id. Halifax 90, Montreal 91, Ottowa 92, Quebec City 93, Toronto 94, Vancouver is 95

**-t** Retry timeout in seconds. Keep this above 60 seconds to make sure you are getting temporarily banned from receiving available dates

# Tips
Comment line 100 and uncomment line 102 in usappointment.js to see puppeteer in action
