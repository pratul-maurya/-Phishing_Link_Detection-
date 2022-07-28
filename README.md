# -Phishing_Link_Detection-
Checks whether a given link is suspected phishing link or not by comparing it against a set of rules and a universal list of domains

Brief Description – 
In the C++ program I have implemented the following 6 phishing rules. 
1. Long URL to Hide the Suspicious Part (1.1.2) 
Phishers can use long URL to hide the doubtful part in the address bar. 
Rule: 
● URL length < 54 → feature = Legitimate 
● else if URL length ≥ 54 and ≤ 75 → feature = Suspicious 
● otherwise → feature = Phishing 

2. Using URL Shortening Services “TinyURL” (1.1.3)
URL shortening is a method on the “World Wide Web” in which a URL may be made considerably smaller in length and still lead to the required webpage. This is accomplished by means of an “HTTP Redirect” on a domain name that is short, which links to the webpage that has a long URL. 
Rule: 
● TinyURL → Phishing 
● Otherwise → Legitimate 

3. URL’s having “@” Symbol (1.1.4)
Using “@” symbol in the URL leads the browser to ignore everything preceding the “@” symbol and the real address often follows the “@” symbol. 
Rule: 
● Url Having @ Symbol → Phishing 
● Otherwise → Legitimate

4. Redirecting using “//” (1.1.5)
The existence of “//” within the URL path means that the user will be redirected to another website. An example of such URL’s is: http://www.legitimate.com//http://www.phishing.com”. We examine the location where the “//” appears. 
Rule: 
● The Position of the Last Occurrence of "//" in the URL > 7 → Phishing
● Otherwise → Legitimate

5. Adding Prefix or Suffix Separated by (-) to the Domain (1.1.6)
The dash symbol is rarely used in legitimate URLs. Phishers tend to add prefixes or suffixes separated by (-) to the domain name so that users feel that they are dealing with a legitimate webpage. 
Rule: 
● Domain Name Part Includes (−) Symbol → Phishing 
● Otherwise → Legitimate

6. The Existence of “HTTPS” Token in the Domain Part of the URL (1.1.12)
The phishers may add the “HTTPS” token to the domain part of a URL in order to trick users. 
Rule: 
● Using HTTP Token in Domain Part of The URL → Phishing /n
● Otherwise → Legitimate/n

The python program checks the given URL for the following 2 phishing rules: 
7. Domain Registration Length (1.1.9)
Based on the fact that a phishing website lives for a short period of time, we believe that trustworthy domains are regularly paid for several years in advance. 
Rule: 
● Domains Expires on ≤ 1 years → Phishing 
● Otherwise → Legitimate

8. Abnormal URL (1.2.6)
This feature can be extracted from WHOIS database. For a legitimate website, identity is typically part of its URL. 
Rule: 
● The Host Name Is Not Included In URL → Phishing 
● Otherwise → Legitimate

Screenshots of output –

![image](https://user-images.githubusercontent.com/70075276/181445605-3f878c6a-78d3-43f8-b8ff-6f662873325c.png)
![image](https://user-images.githubusercontent.com/70075276/181445674-0961056f-2f03-485d-98ed-89fa244eb192.png)
![image](https://user-images.githubusercontent.com/70075276/181445693-f88214a6-fb93-4f50-8324-e637e74424ea.png)

![image](https://user-images.githubusercontent.com/70075276/181445721-6e1dd936-21b4-4200-93dd-65e2896a2c3a.png)
