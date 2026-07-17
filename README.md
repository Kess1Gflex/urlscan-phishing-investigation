# URLScan.io Phishing Investigation

## Project Overview

This project demonstrates my ability to perform web and phishing investigations using URLScan.io in a simulated Security Operations Center (SOC) environment.

The objective was to analyze a publicly available website, review its infrastructure, identify indicators of compromise (IOCs), and determine whether there was sufficient evidence to classify the website as suspicious or malicious.

This investigation reflects the type of initial triage and analysis that a Tier 1 SOC Analyst would perform when responding to alerts involving suspicious links submitted by employees or detected by email security solutions.

---

## Scenario

A SOC analyst receives an alert indicating that an employee accessed the following website:

> `https://electronicsmartly.com`

Management requests an initial assessment to determine whether the website exhibits signs of phishing, malicious activity, or suspicious infrastructure.

---

## Investigation Objectives

* Determine whether the domain is suspicious.
* Review the website's appearance and page title.
* Identify the domain's age and registrar.
* Analyze contacted domains and IP addresses.
* Assess whether there is evidence of phishing.
* Document findings and provide a recommendation.

---

## Tool Used

| Tool       | Purpose                             |
| ---------- | ----------------------------------- |
| URLScan.io | Website and infrastructure analysis |

---

## Investigation Process

### Step 1: Submit URL to URLScan.io

The URL was submitted to URLScan.io for analysis.

**URL Submitted:**

```text
https://electronicsmartly.com
```

---

### Step 2: Review Screenshot

The first step during URL investigations is determining what the user would have seen.

Observation:

* Website displayed electronics-related content.
* No login prompts were observed.
* No signs of brand impersonation were identified.

> SOC Note: A mismatch between the page title and the domain is often an indicator of phishing.

---

### Step 3: Review Page Title

| Field      | Value                                             |
| ---------- | ------------------------------------------------- |
| Page Title | Shop Cutting-Edge Wearable Tech Innovations Today |

Analysis:

* The title aligns with the website's purpose.
* No evidence of impersonation of Microsoft, Google, PayPal, or banking institutions.

---

### Step 4: Review Domain Information

| Field      | Value                 |
| ---------- | --------------------- |
| Domain     | electronicsmartly.com |
| Registrar  | NAMECHEAP INC         |
| Domain Age | Approximately 2 Years |

Analysis:

* The domain is not newly registered.
* Newly created domains are commonly observed in phishing campaigns.
* Domain age does not indicate immediate concern.

---

### Step 5: Review Infrastructure

The following IP addresses were identified during the investigation:

| IP Address      | Provider                |
| --------------- | ----------------------- |
| 185.111.111.154 | CDNEXT Datacamp Limited |
| 172.67.197.50   | Cloudflare              |
| 185.111.111.159 | CDNEXT Datacamp Limited |
| 34.23.59.145    | Google Cloud Platform   |

Analysis:

* The website utilizes known infrastructure providers.
* Cloudflare and Google Cloud are commonly used by legitimate organizations.
* No immediately suspicious infrastructure was observed.

---

### Step 6: Review Contacted Domains

| Domain                     | Purpose           |
| -------------------------- | ----------------- |
| electronicsmartly.com      | Primary website   |
| cdn.freshstore.cloud       | Content delivery  |
| analytics.freshstore.cloud | Analytics         |
| rsms.me                    | External resource |

Analysis:

* Contacted domains appear related to content delivery and analytics.
* No obvious indicators of malicious infrastructure were identified.

---

### Indicators of Compromise (IOCs)

| IOC Type   | Value                 |
| ---------- | --------------------- |
| Domain     | electronicsmartly.com |
| IP Address | 185.111.111.154       |
| IP Address | 172.67.197.50         |
| IP Address | 185.111.111.159       |
| IP Address | 34.23.59.145          |

---

## Analyst Assessment

| Question                   | Assessment |
| -------------------------- | ---------- |
| Domain and title match?    | Yes        |
| Recently registered?       | No         |
| Evidence of impersonation? | No         |
| Suspicious infrastructure? | No         |
| Malicious classification?  | No         |

---

## Final Verdict

Based on the available URLScan.io data, there were no obvious indicators of phishing or malicious activity observed during the investigation.

The website's title aligned with the registered domain, the infrastructure appeared legitimate, and the domain had been active for approximately two years.

At the time of analysis, there was insufficient evidence to classify the website as malicious.

> Analyst Statement:
>
> "No indicators of compromise or phishing activity were observed during the initial triage. Continued monitoring is recommended if additional intelligence becomes available."

---

## Key Takeaways

This project reinforced several SOC concepts:

* Domain analysis
* Title-domain mismatch identification
* IOC identification
* Infrastructure analysis
* Initial phishing triage
* Website legitimacy assessment

---

## Skills Demonstrated

* Security Operations (SOC)
* Threat Intelligence
* URL Investigation
* IOC Analysis
* Phishing Analysis
* Technical Documentation
* Cybersecurity Reporting

---

## Screenshots

### URLScan Overview

```text
Replace with:
/screenshots/01-overview.png
```

### Screenshot Analysis

```text
Replace with:
/screenshots/02-screenshot.png
```

### Domain Information

```text
Replace with:
/screenshots/03-domain-info.png
```

### Contacted Domains

```text
Replace with:
/screenshots/04-contacted-domains.png
```

### IP Analysis

```text
Replace with:
/screenshots/05-ip-addresses.png
```

### Final Assessment

```text
Replace with:
/screenshots/06-final-assessment.png
```

---

## Future Improvements

* Integrate VirusTotal URL analysis.
* Correlate findings with AbuseIPDB.
* Expand investigation using Shodan.
* Compare findings with Cisco Talos Intelligence.
* Automate IOC collection using Python.

---

## Author

**Blessing O.**

Aspiring SOC Analyst with interests in Threat Intelligence, Incident Response, and Security Operations.

LinkedIn: `[INSERT LINK]`

GitHub: `[INSERT LINK]`
