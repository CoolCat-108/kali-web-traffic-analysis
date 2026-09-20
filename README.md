# kali-web-traffic-analysis
A controlled web-application traffic analysis lab using Kali Linux, Burp Suite, Wireshark, and OWASP Juice Shop.
# Web Application Traffic Analysis Lab

## Project Overview

This project demonstrates web-application and network-traffic analysis
in an isolated Kali Linux laboratory. I used Burp Suite to inspect HTTP
requests and responses and Wireshark to capture and analyze the associated
network traffic.

## Objectives

- Build an isolated cybersecurity testing environment
- Intercept HTTP requests with Burp Suite
- Capture network traffic with Wireshark
- Correlate web requests with network packets
- Document a security observation
- Recommend an appropriate mitigation

## Tools Used

- Kali Linux
- OWASP Juice Shop
- Burp Suite Community Edition
- Wireshark
- Firefox
- Markdown

## Scope and Authorization

All testing was conducted against OWASP Juice Shop running locally in an
isolated laboratory. OWASP Juice Shop is an intentionally vulnerable
training application. No third-party or production systems were tested.

## Lab Architecture

The laboratory contained:

1. Kali Linux as the primary operating system
2. OWASP Juice Shop as the local target application
3. Burp Suite as the HTTP interception proxy
4. Wireshark as the network-packet analyzer

## Methodology

1. Started the local OWASP Juice Shop application.
2. Captured normal application traffic in Wireshark.
3. Opened the application through Burp Suite's browser.
4. Intercepted and reviewed an HTTP request.
5. Examined the corresponding HTTP response.
6. Located the related network conversation in Wireshark.
7. Documented the security-relevant observations.
8. Sanitized all evidence before publication.

## Security Finding

### Title

Excessive Information Exposure in an HTTP Response

### Description

The selected response contained implementation information that was not
necessary for normal client operation.

### Risk

Unnecessary implementation details may help an attacker understand the
application's architecture or identify technologies for further research.

### Recommendation

Remove unnecessary diagnostic and technology-identifying information from
production responses. Return only the information required by the client.

### Severity

Informational or Low

## Evidence

Add sanitized screenshots showing:

- The local laboratory environment
- Burp Suite HTTP history
- The selected HTTP request and response
- The corresponding Wireshark traffic
- Relevant packet filters

## Skills Demonstrated

- HTTP request and response analysis
- Burp Suite proxy operation
- Wireshark packet analysis
- Network display filtering
- Evidence collection
- Data sanitization
- Security risk assessment
- Technical report writing

## Lessons Learned

This project helped me understand the relationship between application-layer
HTTP activity and the underlying network traffic. Burp Suite provided a
focused view of web requests and responses, while Wireshark provided packet
and connection context.

## Ethical Statement

This project was completed exclusively in an authorized local laboratory
using an intentionally vulnerable training application.
