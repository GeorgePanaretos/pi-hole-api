# PI-hole (DNS Monitor and Blocker) API Calls

## Overview
This repository contains a collection of API calls for managing and monitoring your PI-hole DNS server. PI-hole is a network-wide ad blocker that blocks ads at the DNS level, providing a streamlined and ad-free browsing experience across your entire network.

## Purpose
This collection enables you to automate the management of your PI-hole server, integrate it with other systems, and streamline your ad-blocking configuration. The provided API calls cover various functionalities, including managing blacklists and whitelists, enabling or disabling domains, and retrieving system statistics.

## Schema
The collection is structured according to the Postman Collection v2.1.0 schema.

## API Endpoints

### 1. Get version (no auth)
- **Description**: Retrieves the current version of the PI-hole.
- **Method**: GET
- **URL**: `http://{{pihole}}/admin/api.php?version`
- **Headers**: None

### 2. Summary info formatted (auth)
- **Description**: Retrieves a summary of PI-hole statistics in a formatted manner.
- **Method**: GET
- **URL**: `http://{{pihole}}/admin/api.php?summary&auth={{piholetoken}}`
- **Headers**: None

### 3. Summary statistics info in raw format (auth)
- **Description**: Retrieves raw summary statistics of PI-hole.
- **Method**: GET
- **URL**: `http://{{pihole}}/admin/api.php?summaryRaw&auth={{piholetoken}}`
- **Headers**: None

### 4. Backend type (no auth)
- **Description**: Retrieves the backend type of the PI-hole.
- **Method**: GET
- **URL**: `http://{{pihole}}/admin/api.php?type`
- **Headers**: None

### 5. Stats data last 10 minutes (auth)
- **Description**: Retrieves PI-hole statistics for the last 10 minutes.
- **Method**: GET
- **URL**: `http://{{pihole}}/admin/api.php?overTimeData10mins&auth={{piholetoken}}`
- **Headers**: None

### 6. Get recentBlocked (auth)
- **Description**: Retrieves the most recently blocked domains.
- **Method**: GET
- **URL**: `http://{{pihole}}/admin/api.php?recentBlocked&auth={{piholetoken}}`
- **Headers**: None

### 7. Get top 10 items list (auth)
- **Description**: Retrieves the top 10 queried items.
- **Method**: GET
- **URL**: `http://{{pihole}}/admin/api.php?topItems=10&auth={{piholetoken}}`
- **Headers**: None

### 8. Get query sources (auth)
- **Description**: Retrieves the sources of queries.
- **Method**: GET
- **URL**: `http://{{pihole}}/admin/api.php?getQuerySources=100&auth={{piholetoken}}`
- **Headers**: None

### 9. Top blocked sources (auth)
- **Description**: Retrieves the top blocked sources.
- **Method**: GET
- **URL**: `http://{{pihole}}/admin/api.php?topClientsBlocked&auth={{piholetoken}}`
- **Headers**: None

### 10. Top queries and ads (auth)
- **Description**: Retrieves the top queries and ads.
- **Method**: GET
- **URL**: `http://{{pihole}}/admin/api.php?topItems&auth={{piholetoken}}`
- **Headers**: None

### 11. Top clients dynamic (auth)
- **Description**: Retrieves the top clients dynamically.
- **Method**: GET
- **URL**: `http://{{pihole}}/admin/api.php?topClients=10&auth={{piholetoken}}`
- **Headers**: None

### 12. Top clients static default 10 (auth)
- **Description**: Retrieves the top clients (default 10).
- **Method**: GET
- **URL**: `http://{{pihole}}/admin/api.php?topClients&auth={{piholetoken}}`
- **Headers**: None

### 13. Get query type percentages (auth)
- **Description**: Retrieves the percentages of query types.
- **Method**: GET
- **URL**: `http://{{pihole}}/admin/api.php?getQueryTypes&auth={{piholetoken}}`
- **Headers**: None

### 14. Get all queries (auth)
- **Description**: Retrieves all queries.
- **Method**: GET
- **URL**: `http://{{pihole}}/admin/api.php?getAllQueries&auth={{piholetoken}}`
- **Headers**: None

### 15. Get forwarding destinations (auth)
- **Description**: Retrieves the forwarding destinations.
- **Method**: GET
- **URL**: `http://{{pihole}}/admin/api.php?getForwardDestinations&auth={{piholetoken}}`
- **Headers**: None

### 16. Get forwarding destinations count (auth)
- **Description**: Retrieves the count of forwarding destinations.
- **Method**: GET
- **URL**: `http://{{pihole}}/admin/api.php?getForwardDestinations=10&auth={{piholetoken}}`
- **Headers**: None

### 17. Get cache info (auth)
- **Description**: Retrieves cache information.
- **Method**: GET
- **URL**: `http://{{pihole}}/admin/api.php?getCacheInfo&auth={{piholetoken}}`
- **Headers**: None

### 18. Get over time data clients (auth)
- **Description**: Retrieves over time data for clients.
- **Method**: GET
- **URL**: `http://{{pihole}}/admin/api.php?overTimeDataClients&auth={{piholetoken}}`
- **Headers**: None

### 19. Add site to black list
- **Description**: Adds a site to the blacklist.
- **Method**: GET
- **URL**: `http://{{pihole}}/admin/api.php?list=black&add=badsite.com&auth={{piholetoken}}`
- **Headers**: None

### 20. Delete site from black list
- **Description**: Deletes a site from the blacklist.
- **Method**: GET
- **URL**: `http://{{pihole}}/admin/api.php?list=black&sub=badsite.com&auth={{piholetoken}}`
- **Headers**: None

### 21. Add site to white list
- **Description**: Adds a site to the whitelist.
- **Method**: GET
- **URL**: `http://{{pihole}}/admin/api.php?list=white&add=goodsite.com&auth={{piholetoken}}`
- **Headers**: None

### 22. Delete site from white list
- **Description**: Deletes a site from the whitelist.
- **Method**: GET
- **URL**: `http://{{pihole}}/admin/api.php?list=white&sub=goodsite.com&auth={{piholetoken}}`
- **Headers**: None

### 23. Get status (Enabled/Disabled)
- **Description**: Retrieves the current status (Enabled/Disabled) of PI-hole.
- **Method**: GET
- **URL**: `http://{{pihole}}/admin/api.php?status&auth={{piholetoken}}`
- **Headers**: None

### 24. Disable
- **Description**: Disables PI-hole.
- **Method**: GET
- **URL**: `http://{{pihole}}/admin/api.php?disable&auth={{piholetoken}}`
- **Headers**: None

### 25. Disable for XX seconds
- **Description**: Disables PI-hole for a specified number of seconds.
- **Method**: GET
- **URL**: `http://{{pihole}}/admin/api.php?disable=20&auth={{piholetoken}}`
- **Headers**: None

### 26. Enable
- **Description**: Enables PI-hole.
- **Method**: GET
- **URL**: `http://{{pihole}}/admin/api.php?enable&auth={{piholetoken}}`
- **Headers**: None

## How to Use

1. **Import the Collection**:
   - Download the Postman collection JSON file and import it into your Postman app.

2. **Configure Environment**:
   - Set up your environment variables such as `pihole` and `piholetoken` to match your PI-hole instance.

3. **Execute Requests**:
   - Use the various requests in the collection to manage your PI-hole server, adjusting parameters as needed.

### Importing in Postman

This collection includes a set of API calls for managing and monitoring a PI-hole DNS server. PI-hole is a network-wide ad blocker that helps to block ads at the DNS level. The collection features endpoints to add or remove domains from blacklists and whitelists, enable or disable domains, and perform various administrative tasks. These API calls enable you to automate and streamline the configuration and management of your PI-hole instance.

