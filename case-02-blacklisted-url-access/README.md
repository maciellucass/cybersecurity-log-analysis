# Case 02 - Blacklisted URL Access

## Alert Overview

An alert was triggered when a user attempted to access an external URL that is listed in the organization's blacklist or threat intelligence feeds. The firewall successfully blocked the request, preventing the connection.

## Alert Information

- Event ID: 8816  
- Alert Rule: Access to Blacklisted External URL Blocked by Firewall  
- Severity: High  
- Date: Sep 19th 2026 13:15  
- Data Source: Firewall  

## Alert Visualization

![Alert Screenshot](case-02-blacklisted-url-access-screenshot.png)

## Affected Entities

- Source IP: 10.20.2.17  
- Destination IP: 67.199.248.11  
- URL: http://bit.ly/3sHkX3da12340  

## Investigation

The analysis of the firewall logs shows that an internal host attempted to access a shortened URL (bit.ly), which is commonly used to obfuscate malicious destinations.

Key findings:

- The request was blocked by the firewall (Action: blocked)
- The destination domain is associated with known malicious activity
- URL shortening services were used to hide the final destination
- The traffic was identified as web browsing over TCP (port 80)

These indicators suggest a potential phishing attempt or user interaction with a malicious link.

## Conclusion

The firewall successfully prevented access to a blacklisted URL, mitigating the potential threat before it could impact the system. However, the attempt indicates that a user may have interacted with a suspicious or malicious link.

## Recommendations

- Investigate the source host for potential compromise
- Educate users about phishing and malicious links
- Consider blocking or monitoring URL shortening services
- Review endpoint logs for additional suspicious activity

## Disclaimer

This analysis was conducted in a controlled lab environment for educational purposes using TryHackMe. No real systems were impacted.
