# Case 02 - Phishing Email Analysis

## Overview

An alert was triggered for a suspicious inbound email containing a potentially malicious link. The email exhibited clear phishing characteristics, aiming to trick the user into entering credentials on a fake login page.

---

## Affected Entities

- User: c.allen
- Sender: no-reply@m1crosoftsupport.co
- Malicious Domain: m1crosoftsupport.co
- Email Theme: Unusual Sign-In Activity

---

## Investigation

The email was analyzed and identified as a phishing attempt based on multiple indicators:

- The sender domain is a spoofed version of a legitimate Microsoft domain
- The domain uses character substitution ("1" instead of "i")
- The email contains urgency tactics to pressure the user
- A malicious link redirects to a fake login page

No evidence of user interaction (click or credential submission) was found.

---

## Evidence

The screenshot below shows the phishing email identified during analysis:

![Phishing Email](../screenshots/case-02-phishing-email-analysis-screenshot.png)

---

## Classification

True Positive – Phishing Attempt

---

## Reason for Classification

The alert was triggered by a suspicious email containing a spoofed domain and a malicious link. The domain mimics a legitimate service using a common phishing technique (character substitution).

---

## Recommended Actions

- Block the domain at the email gateway
- Add the sender to the blacklist
- Notify the user about the phishing attempt
- Conduct awareness training
- Monitor for similar phishing attempts

---

## Indicators of Compromise (IOCs)

- m1crosoftsupport.co
- no-reply@m1crosoftsupport.co
