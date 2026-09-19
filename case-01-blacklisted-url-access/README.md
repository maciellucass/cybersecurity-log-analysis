# Case 01 - Blacklisted URL Access

## Overview

An alert was triggered indicating that a user attempted to access a known malicious or blacklisted URL.

---

## Affected Entities

- User: j.doe
- Source IP: 192.168.1.10
- Destination URL: http://malicious-site.com

---

## Investigation

- URL confirmed as malicious via threat intelligence
- No download detected
- No suspicious execution observed

---

## Classification

True Positive – Suspicious Activity

---

## Recommended Actions

- Block domain
- Monitor user activity
- Run endpoint scan
