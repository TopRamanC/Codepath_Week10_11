# Codepath_Week10_11
MHN Admin Deployment: 

Dionaea Honeypot Deployment: For the Honeypot instance I also used gcloud to make firewall rules and the instance for the Honeypot VM. Then, I copied the "Deploy Command" from MHN Admin browser window and paste it into the Honeypot VM through ssh. Then, the Honeypot was available in the "Sensors" tab and I just waited a few days and waited for people to attack it.

Data Bakup (session.json): 

# Honeypot Assignment

**Time spent:** **24** hours spent in total

**Objective:** Create a honeynet using MHN-Admin. Present your findings as if you were requested to give a brief report of the current state of Internet security. Assume that your audience is a current employer who is questioning why the company should allocate anymore resources to the IT security team.

### MHN-Admin Deployment (Required)

**Summary:** How did you deploy it? Did you use GCP, AWS, Azure, Vagrant, VirtualBox, etc.?
Using Gcloud command line I made the firewall rules for MHN-Admin and then also made the instance "MHN-Admin". Then, I used the gcloud ommand line to ssh to MHN-Admin where I followed the procedure to install the MHN Admin Application.

![mhn-admin](https://user-images.githubusercontent.com/76242390/116630644-6d172d00-a908-11eb-9314-3d17b61e6bdb.gif)

### Dionaea Honeypot Deployment (Required)

**Summary:** Briefly in your own words, what does dionaea do?
- Dionaea captures attacks payloads and malware.

![Honeypot](https://user-images.githubusercontent.com/76242390/116628281-a26d4c00-a903-11eb-987b-fe9ad0d361dd.gif)



### Database Backup (Required) 

**Summary:** What is the RDBMS that MHN-Admin uses? What information does the exported JSON file record?
- MHN-Admin uses MongoDB. The exported JSON file recorded attack logs with IP address, port numbers, etc...from the people that attacked my honeypot. 

Summary: To download the session.json file I made a ssh connection to MHN Admin from the browser window and then I ran the following commands to export the file, make the size smaller, and then save it to my Host machine.
1. mongoexport --db mnemosyne --collection session > session.json (Used this to export the file)
2. truncate --size="<5M" session.json (Used this to make the file size smaller)
3. readlink -e session.json (Used this command to download the file to my computer)

![database backup](https://user-images.githubusercontent.com/76242390/116627362-d6e00880-a901-11eb-8a78-b569db128d0f.gif)

*Be sure to upload session.json directly to this GitHub repo/branch in order to get full credit.*



## Notes

Describe any challenges encountered while doing the assignment.
The challenges I faced were mainly following the instructions from codepath as I believe some of them were not correct but CodePath was able to update the instructions and then I was able to finsih the assigment. 
