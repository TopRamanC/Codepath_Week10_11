# Codepath_Week10_11
MHN Admin Deployment: Using Gcloud command line I made the firewall rules for MHN-Admin and then also made the instance "MHN-Admin". Then, I used the gcloud ommand line to ssh to MHN-Admin where I followed the procedure to install the MHN Admin Application.

Dionaea Honeypot Deployment: For the Honeypot instance I also used gcloud to make firewall rules and the instance for the Honeypot VM. Then, I copied the "Deploy Command" from MHN Admin browser window and paste it into the Honeypot VM through ssh. Then, the Honeypot was available in the "Sensors" tab and I just waited a few days and waited for people to attack it.

Data Bakup (session.json): To download the session.json file I made a ssh connection to MHN Admin from the browser window and then I ran the following commands to export the file, make the size smaller, and then save it to my Host machine.
1. mongoexport --db mnemosyne --collection session > session.json (Used this to export the file)
2. truncate --size="<5M" session.json (Used this to make the file size smaller)
3. readlink -e session.json (Used this command to download the file to my computer)
