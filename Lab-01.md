# Lab 01: Enterprise Infrastructure Audit
**Date:** January 30, 2026  
**Status:** Completed  

## 🎯 Objective
Analyze the October 2021 Facebook outage from a systems/network perspective and identify how BGP routing changes can take a large service offline.

## 🛠️ Tools Used
- Web browser (research + reading technical breakdowns)
- Notes (writing findings clearly)
- Wireshark (concept connection: how routing issues affect traffic visibility)

## 🔍 Key Findings
1. **Root Cause (High level):** A network configuration change caused Facebook’s BGP routes to disappear, so the internet could not find Facebook’s DNS/services.
2. **Why users felt it immediately:** If DNS can’t be reached, apps and websites can’t load even if servers still exist.
3. **Cascading failure (operational impact):** Internal systems were disrupted because staff depend on the same network identity and tooling to access systems and facilities.

## 💡 Lessons Learned
- BGP and DNS are “critical infrastructure” for availability. If routing breaks, the product (uptime) disappears.
- Large environments need safer change controls for network updates (review, staged rollout, and rollback plans).
- Out-of-band access and resilient internal tooling reduce downtime when primary networks fail.

## 📸 Proof of Work
- Screenshot 1: Notes showing the BGP/DNS cause-and-effect summary
- Screenshot 2: Timeline summary of what failed first and what failed next

![Lab 01 Notes Screenshot](proof/lab-01-notes.png)
![Outage Timeline Screenshot](proof/lab-01-timeline.png)
