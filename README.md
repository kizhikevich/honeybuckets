# honeybuckets

This GitHub repository hosts the data collected by our honeypot experiment, including the SSH Cowrie logs and the built-in AWS logs. A few important notes: 
1) The raw SSH logs are found in ```SSH_Honeypot/CFAA_Violation_2022_23``` and ```SSH_Honeypot/Data_2022```. ```SSH_Honeypot/Data_2022``` contains every SSH attempt to our honeypot every day from 09-20-2022 to 11-18-2022, including days where our credentials were used (indicating the traffic came from our buckets and/or a colluding actor). ```SSH_Honeypot/CFAA_Violation_2022_23``` includes every SSH attempt to our honeypot *only* on days where our credentials were used.
2) Our study had two parts: pilot and company study. In ```Bucket_Logs/``` I separate the AWS s3 logs for both. The data in this repository goes beyond what was included in the study, so numbers reported in the paper may not align exactly with the data.
3) In the ```Bucket_Logs/Pilot/alphanumeric_buckets.py``` there are functions in the file defining which alphanumeric buckets were used for our control and which buckets were used for our leaked sets (and where they were leaked). Note: some alphanumeric buckets in our logs were never used for analysis-- these are just like the controls, meaning they are not leaked anywhere. 
To cite our paper, please use the following citation:

```
Katherine Izhikevich, Geoffrey M. Voelker, Stefan Savage, Liz Izhikevich. Using Honeybuckets to Characterize Cloud
Storage Scanning in the Wild. In Proceedings of the 9th IEEE European Symposium on Security and Privacy, Vienna,
Austria, July 2024.
```
