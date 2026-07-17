# URLScan.io Phishing Investigation

## Project Overview

This repository documents a phishing triage exercise performed using URLScan.io.

The goal of this investigation was to determine whether a reported website exhibited indicators commonly associated with phishing campaigns, including domain impersonation, suspicious infrastructure, and malicious network relationships.

This project simulates the responsibilities of a Tier 1 Security Operations Center (SOC) Analyst responding to a user-submitted suspicious URL.

---

## Scenario

At 9:12 AM, an employee reported receiving a link from an external source and requested assistance verifying its legitimacy.

The employee stated:

> "I clicked on a website selling electronics products. It didn't ask me to log in, but I want to confirm whether it is safe."

The reported URL was:

```text
https://electronicsmartly.com
```

The SOC team was tasked with performing an initial investigation and documenting its findings.

---

## Investigation Workflow

1. Submit URL to URLScan.io.
2. Review website appearance.
3. Analyze page title.
4. Review domain registration details.
5. Analyze contacted domains.
6. Review associated IP addresses.
7. Determine whether sufficient evidence exists to classify the URL as malicious.
8. Provide an analyst recommendation.

---

## Tool Used

| Tool       | Purpose                             |
| ---------- | ----------------------------------- |
| URLScan.io | Website and infrastructure analysis |

---

## Step 1: Submit URL to URLScan.io

The URL was submitted to URLScan.io to collect intelligence regarding its infrastructure and behavior.

### URL Submitted

```text
https://electronicsmartly.com
```

### Analyst Observation

The submission completed successfully and returned a full infrastructure report for the domain.

### Screenshot

<img src="screenshots/01-url-submission.png" width="900">

---

## Step 2: Review Website Appearance

The first step in any phishing investigation is understanding what the end user saw.

URLScan generated a screenshot of the website during analysis.

### Findings

* Electronics-themed website.
* No login page observed.
* No credential request observed.
* No evidence of banking or Microsoft impersonation.

### Analyst Note

One of the quickest phishing indicators is a mismatch between the domain name and the content displayed to the user.

For example:

* `microsoft-security-login.com`
* `paypal-secure-update.net`
* `apple-account-verify.org`

No such mismatch was identified during this investigation.

### Screenshot

<img src="screenshots/02-website-screenshot.png" width="900">

---

## Step 3: Review Page Title

The page title was analyzed to determine whether the website was attempting to impersonate another organization.

| Field      | Value                                             |
| ---------- | ------------------------------------------------- |
| Domain     | electronicsmartly.com                             |
| Page Title | Shop Cutting-Edge Wearable Tech Innovations Today |

### Findings

* Title aligned with website content.
* No evidence of impersonation.
* No references to financial institutions or technology companies.

### Analyst Assessment

At this stage, the website did not exhibit characteristics commonly observed in phishing campaigns.

### Screenshot

<img src="screenshots/03-page-title.png" width="900">

---

## Step 4: Review Domain Information

The next step involved reviewing registration details.

| Field          | Value                 |
| -------------- | --------------------- |
| Registrar      | NAMECHEAP INC         |
| Domain Created | October 31, 2024      |
| Domain Age     | Approximately 2 Years |

### Findings

* Domain is not newly created.
* Older domains generally carry lower phishing risk.
* Registrar is widely used and reputable.

### Analyst Assessment

Threat actors frequently leverage domains registered within the previous 30 days. This domain did not meet that criterion.

### Screenshot

<img src="screenshots/04-domain-information.png" width="900">

---

## Step 5: Analyze Contacted Domains

URLScan identified several domains contacted during page rendering.

| Domain                     |
| -------------------------- |
| electronicsmartly.com      |
| cdn.freshstore.cloud       |
| analytics.freshstore.cloud |
| rsms.me                    |

### Findings

* Supporting domains appeared to provide analytics and content delivery services.
* No known malicious domains were identified during initial triage.

### Analyst Assessment

Contacted domains are important because they reveal third-party relationships that may indicate tracking services, malware delivery, or command-and-control activity.

### Screenshot

<img src="screenshots/05-contacted-domains.png" width="900">

---

## Step 6: Analyze IP Addresses

The following infrastructure was identified:

| IP Address      | Provider                |
| --------------- | ----------------------- |
| 185.111.111.154 | CDNEXT Datacamp Limited |
| 172.67.197.50   | Cloudflare              |
| 185.111.111.159 | CDNEXT Datacamp Limited |
| 34.23.59.145    | Google Cloud Platform   |

### Findings

* Cloudflare infrastructure identified.
* Google Cloud infrastructure identified.
* No immediately suspicious hosting providers observed.

### Analyst Assessment

IP addresses alone are not sufficient to determine maliciousness because threat actors frequently rotate infrastructure. However, IP intelligence provides useful context during investigations.

### Screenshot

<img src="screenshots/06-ip-analysis.png" width="900">

---

## Step 7: IOC Collection

The following Indicators of Compromise (IOCs) were collected during the investigation.

| Type   | Value                 |
| ------ | --------------------- |
| Domain | electronicsmartly.com |
| IP     | 185.111.111.154       |
| IP     | 172.67.197.50         |
| IP     | 185.111.111.159       |
| IP     | 34.23.59.145          |

### Screenshot

<img src="screenshots/07-ioc-table.png" width="900">

---

## Final Analyst Verdict

After reviewing the available evidence, the domain did not demonstrate sufficient indicators to classify it as malicious.

### Summary

| Question                           | Result |
| ---------------------------------- | ------ |
| Domain impersonation detected?     | No     |
| Suspicious page title?             | No     |
| Newly registered domain?           | No     |
| Malicious infrastructure observed? | No     |
| Evidence of phishing?              | No     |

### Final Recommendation

> No evidence of phishing or malicious activity was identified during initial triage. Continue monitoring if additional intelligence becomes available.

### Screenshot

<img src="screenshots/08-final-verdict.png" width="900">

---

## Skills Demonstrated

* Security Operations Center (SOC) Analysis
* URL Investigation
* Threat Intelligence
* IOC Collection
* Infrastructure Analysis
* Phishing Triage
* Incident Documentation
* Technical Reporting

---

## Key Lessons Learned

This investigation reinforced several important concepts:

* Domains should always be read from right to left.
* A title-domain mismatch is a common phishing indicator.
* Domain age can provide valuable investigative context.
* IP addresses may change and should not be treated as sole evidence.
* IOC collection is a critical SOC responsibility.
* Documentation is as important as technical analysis.


---

## Author

**Blessing O.**

Aspiring SOC Analyst passionate about Security Operations, Threat Intelligence, and Incident Response.

* LinkedIn: www.linkedin.com/in/ogburogho-blessing-22376b23a
* GitHub: https://github.com/Kess1Gflex
