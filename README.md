#
# Azion SE Assessment — Guilherme França
#
This repository contains the configuration, testing evidence, and documentation for the Azion Solutions Engineer technical assessment.

# Objective
Configure https://httpbingo.org as a reverse proxy on Azion's edge platform, applying targeted WAF protection on the '/login' endpoint, bypassing security inspection for static assets, and implementing aggressive caching for performance and cost optimization.

# Live Domain
https://fklsxzla7sy.map.azionedge.net

# What Was Configured

- Edge Application with Application Accelerator for advanced caching and rules
- Connector pointing to httpbingo.org over forced HTTPS
- WAF enabled only created on /login (GET and POST), blocking SQLi, XSS, RFI, RCE, Directory Traversal, Evading Tricks and Identified Attacks
- Rate limiting on /login
- WAF bypass for static assets
- Cache TTL of 30 days for static files and 0s for '/login'
- Gzip compression for static text-based assets
