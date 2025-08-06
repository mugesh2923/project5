# project5
# Security Log Analysis using Splunk SIEM

## Tool used
1.splunk
2.ssh,http,dns log files
3.github

## 🔍 Project Summary

This project focuses on analyzing real-world security log data using Splunk. The goal is to detect suspicious activities such as web scanning, brute force SSH login attempts, and abnormal DNS behavior using custom SPL (Search Processing Language) queries. 

By uploading and analyzing HTTP, DNS, and SSH logs in Splunk, we identified attack patterns and created queries to detect them. This project is aimed at demonstrating hands-on log analysis skills required for a SOC Analyst role.

---

## 🗂️ Log Sources Used

- **HTTP Access Logs**  
  To table the log like host ip & port ,destination ip & port etc...and Analyzed repeated 404 errors from the same IP to identify web scanning behavior.

- **DNS Logs**  
  Investigated abnormal DNS query volume from a single source IP (possible beaconing or malware behavior).

- **SSH Authentication Logs**  
  count all event like (succesfull,failure) attempt and Detected brute force attacks repeated failed login attempts from the same IP address 


