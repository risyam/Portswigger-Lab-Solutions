## Username Enumeration

## How to test for username enumeration:

1. Difference in error messages
2. Difference in HTTP status codes 
3. Difference in response times in different scenarios:
    - Repsonse time and length of the password (Repeat the request to ensure the differece in response time)
     

### Bypass IP-based brute-force protection- Method 1
`Use X-Forwarded-For header with any integer or ip value, to spoof the source IP`
 
 `Use Pitchfork in Burp Intruder to iterate over X-forwarded-host header and username parameter`

### Bypass IP-based brute-force protection- Method 2

`Reset the counter for the number of failed login attempts by logging in with a valid credentials (Eg. your own) before this limit is reached.`

Notes: 

1. **On the Resource pool tab, the Maximum concurrent requests should be set to 1**

2. **The list of payloads for usernames should alternate between a valid username and the victim username for password enumeration**
