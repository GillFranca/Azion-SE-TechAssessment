#
# Azion Senior Solutions Engineer Assessment — Guilherme França
#
This repository contains the configuration, testing evidences, and some documentation for the Azion Solutions Engineer technical assessment.

# Objective
THe objective of this assessment was to configure https://httpbingo.org as a reverse proxy on Azion's edge platform, applying WAF protection on the '/login' endpoint, bypassing security inspection for static assets, and implementing aggressive caching for performance and cost optimization.

# Live Domain
https://fklsxzla7sy.map.azionedge.net

# What Was Configured
- Edge Application with Application Accelerator for advanced caching and rules
- Connector pointing to httpbingo.org over HTTPS
- WAF enabled only created on /login (GET and POST), blocking SQLi, XSS, RFI, RCE, Directory Traversal, and Identified Attacks
- Rate limiting on /login
- WAF bypass for static assets
- Cache TTL of 30 days for static files and 0s for '/login'
- Gzip compression for static text-based assets
