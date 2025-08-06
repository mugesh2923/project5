# project5
# Log Monitoring and Alerting using Splunk SIEM

## Tool used
1.splunk
2.ssh,http,dns log files
3.github

## 🔍 Project Summary

This project focuses on analyzing real-world security log data using Splunk. The goal is to detect suspicious activities such as web scanning, brute force SSH login attempts, and abnormal DNS behavior using custom SPL (Search Processing Language) queries. 

By uploading and analyzing HTTP, DNS, and SSH logs in Splunk, we identified attack patterns and created queries to detect them. This project is aimed at demonstrating hands-on log analysis and created alert skills required for a SOC Analyst role.

---

## 🗂️ Log Sources Used

- **HTTP Access Logs**  
  To table the log like host ip & port ,destination ip & port etc...and Analyzed repeated 404 errors from the same IP to identify web scanning behavior.

- **DNS Logs**  
  Investigated abnormal DNS query volume from a single source IP (possible beaconing or malware behavior).

- **SSH Authentication Logs**  
  count all event like (succesfull,failure) attempt and Detected brute force attacks repeated failed login attempts from the same IP address

  # alert system example of ssh bruteforce
  index=ssh_logs "Failed password"
| stats count by src_ip
| where count > 10

create a rule save as and add alert|
Field	                                Value|
Title	                           SSH Brute Force Attempt Detected|
Description	                    Alert if any IP fails SSH login 10+ times|
Alert Type                          	Scheduled|
Time Range	                       Run every 15 minutes|

#  create a Scheduled Alert using this query like:

Run every 15 minutes

Trigger if any IP fails >10 times

Action: Log in Triggered Alerts(splunk ui,email )


 



