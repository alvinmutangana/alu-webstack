# HTTPS SSL

## Description
This project covers configuring SSL termination and HTTPS redirection using HAProxy for a web stack.

## Files

### 0-world_wide_web
Bash script that displays DNS information about subdomains.
- Usage: `./0-world_wide_web domain [subdomain]`
- Example: `./0-world_wide_web alvinmutangana.tech`
- Example: `./0-world_wide_web alvinmutangana.tech web-02`

### 1-haproxy_ssl_termination
HAProxy configuration file that:
- Listens on port 443
- Accepts SSL/HTTPS traffic
- Terminates SSL and forwards to backend web servers

### 2-redirect_http_to_https
HAProxy configuration file that:
- Redirects all HTTP traffic (port 80) to HTTPS
- Returns a 301 Moved Permanently response
- Transparent to the user

## Requirements
- HAProxy 1.5 or higher
- Certbot for SSL certificate generation
- Domain configured with subdomains: www, lb-01, web-01, web-02

## Author
Alvin Mutangana
