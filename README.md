![Languages](https://img.shields.io/github/languages/count/C0nw0nk/Nginx-Lua-Anti-DDoS) ![Top language](https://img.shields.io/github/languages/top/C0nw0nk/Nginx-Lua-Anti-DDoS) ![File size](https://img.shields.io/github/size/C0nw0nk/Nginx-Lua-Anti-DDoS/lua/anti_ddos_challenge.lua)

![Cloudflare I am Under Attack Mode!](https://blog.cloudflare.com/content/images/im_under_attack_page.png.scaled500.png)

# Nginx-Lua-Anti-DDoS

A Anti-DDoS script to protect Nginx web servers using Lua with a Javascript
based authentication puzzle inspired by Cloudflare I am under attack mode I
built my own Anti-DDoS authentication HTML page puzzle intergrating my Lua,
Javascript, HTML and HTTP knowledge.

Mitigate a DDoS attack of any size using my free DDoS protection. Don't get ddos
attacked!

If you're under attack and use my script during the attack, visitors will
receive an interstitial page for about five seconds while I analyze the traffic
to make sure it is a legitimate human visitor.

This can protect you from many different forms of DDoS works with both HTTP and
HTTPS / SSL traffic.

No limit on attack size. Uptime guarantee.

## Features

These are some of the features that this project has thus far.

### Security

- I am Under Attack Mode (DDoS Authentication HTML Page)
- IP Address Whitelist
- IP Subnet Ranges Whitelist
- IP Address Blacklist
- IP Subnet Ranges Blacklist
- User-Agent Whitelist
- User-Agent Blacklist
- Protected area / Restricted access field username / password box to restrict access to sites / paths.

### WAF (Web Application Firewall)

- IPv4 and IPv6 blocking and whitelisting including subnet ranges.
- User-Agent blocking and whitelisting to block bad bots and exploits / scanners.
- Ability to inspect POST Data / Fields and block malicious POST requests / exploits.
- Ability to inspect URL for malicious content SQL/SQI Injections XSS attacks / exploits.
- Ability to inspect query strings and arguements for malicious content / exploits.
- Ability to inspect all Request Headers provided by the client connecting.
- Ability to inspect cookies for exploits.

### Caching Speed and Performance

- Query String Sorting
- Query String Whitelist
- Query String Removal (It is a blacklist but it will just drop / remove the argument from the URL not block the request)
- Minification / Compression of files removing white space and nulled out code / lines JS JavaScript, CSS Stylesheets, HTML etc

### Customization of error pages responses and webpage outputs

- Custom error page interception to replace with your own error pages
- Hide Web application errors such as PHP errorrs MySQL errors it will intercept them and display a custom error page instead of showing visitors sensative information
- Modify webpage outputs to replace contents on pages / files

## Improvements / issues

If you have any bugs issues or problems just [create an issue](https://github.com/melroy89/Nginx-Lua-Anti-DDoS/issues).

If you fork or make any changes to improve this or fix problems please do [make a pull request](https://github.com/melroy89/Nginx-Lua-Anti-DDoS/pulls) for the community who also use this. 

## Usage / Installation

Edit settings inside `anti_ddos_challenge.lua` to cater for your own unique needs or improve my work.

lua/anti_ddos_challenge.lua#L61

Add the Lua file to your Nginx configuration directory:

`nginx/conf/lua/`

Once installed into your `nginx/conf/` directory, add the following section to your HTTP block or it can be in a server or location block depending where you want this script to run. For individual locations the entire server or every single website on the server:

```conf
access_by_lua_file anti_ddos_challenge.lua;
```

See examples below.

### Example nginx.conf

This will run for all websites on the nginx server:

```conf
http {
    access_by_lua_file anti_ddos_challenge.lua;
}
```

This will make it run for this website only:

```conf
server {
    access_by_lua_file anti_ddos_challenge.lua;
}
```

This will run in this location block only:

```conf
location / {
    access_by_lua_file anti_ddos_challenge.lua;
}
```

### Other setup options

For setting up the script to run with Tor .onion services, Cloudflares proxy
services, Configuration options of the script
[view the wiki](https://github.com/C0nw0nk/Nginx-Lua-Anti-DDoS/wiki).

## Requirements

You only need Nginx + Lua to use this. Or use OpenResty.

### Where can you download Nginx + Lua ?

[Openresty provide Nginx + Lua builds](https://openresty.org/en/download.html) for Windows, Linux, docker, etc.

[Nginx4windows has Windows specific builds](http://nginx-win.ecsds.eu/) with Lua.

Or you can download the source code for [Nginx here](https://nginx.org/en/download.html) and compile Nginx yourself with Lua.

## About

I was inspired by Conor McKnight, who created the orginal Lua script (he was inspired by Cloudflare feature "I'm Under Attack Mode" https://www.cloudflare.com/). I was inspired by Cloudflare DDoS protection & mitigation solutions and wanted to create a similar feature in Nginx. Without the need of Nginx Plus.

```sh
If you're under attack and have this feature enabled during the attack, visitors
will receive an interstitial page for about five seconds while we analyze the
traffic to make sure it is a legitimate human visitor.

Advanced DDoS Attack Protection

Unmetered DDoS mitigation to maintain performance and availability

Denial of Service attacks continue to grow in sophistication and force: more
distributed, greater volumes of traffic, and encroaching on the application
layer.

A successful attack increases unnecessary costs on your infrastructure and
IT/security staff. More importantly, it hurts your revenue, customer
satisfaction, and brand.

To combat attacks and stay online, you’ll need a solution that’s resilient
scalable, and intelligent.

Mitigate a DDoS attack of any size or duration, Don't get ddos attacked!
```

I love that feature so much ontop of having it enabled on all my Cloudflare
proxied sites I decided to make it into a feature on my own servers so the
traffic that hits my servers without coming from Cloudflares network is kept in
check and authenticated! (Every little helps right!)

Thank you to @Cloudflare for the inspiration and your community for all the
love, A big thanks to the @openresty community you guys rock Lua rocks you are
all so awesome!

Lets build a better internet together! Where Speed, Privacy, Security and Compression matter!

## Protected attack types

- All Layer 7 Attacks
- Mitigating Historic Attacks
- DoS
- DoS Implications
- DDoS
- All Brute Force Attacks
- Zero day exploits
- Social Engineering
- Rainbow Tables
- Password Cracking Tools
- Password Lists
- Dictionary Attacks
- Time Delay
- Any Hosting Provider
- Any CMS or Custom Website
- Unlimited Attempt Frequency
- Search Attacks
- HTTP Basic Authentication
- HTTP Digest Authentication
- HTML Form Based Authentication
- Mask Attacks
- Rule-Based Search Attacks
- Combinator Attacks
- Botnet Attacks
- Unauthorized IPs
- IP Whitelisting
- Bruter
- THC Hydra
- John the Ripper
- Brutus
- Ophcrack
- unauthorized logins
- Injection
- Broken Authentication and Session Management
- Sensitive Data Exposure
- XML External Entities (XXE)
- Broken Access Control
- Security Misconfiguration
- Cross-Site Scripting (XSS)
- Insecure Deserialization
- Using Components with Known Vulnerabilities
- Insufficient Logging & Monitoring
- And many others…

## Features

### Advanced DDoS Attack Protection

My script gives you Unmetered DDoS mitigation to maintain performance and availability for free
Denial of Service attacks continue to grow in sophistication and force: more distributed, greater volumes of traffic, and encroaching on the application layer.
A successful attack increases unnecessary costs on your infrastructure and IT/security staff. More importantly, it hurts your revenue, customer satisfaction, and brand.
To combat attacks and stay online, you’ll need a solution that’s resilient scalable, and intelligent.

## Common Types of DDoS Attacks

### Block Malicious Bot Abuse

Block abusive bots from damaging Internet properties through content scraping, fraudulent checkout, and account takeover.

### Prevent Customer Data Breach

Prevent attackers from compromising sensitive customer data, such as user credentials, credit card information, and other personally identifiable information.

### Layered Security Defense

layered security approach combines multiple DDoS mitigation capabilities into one service. It prevents disruptions caused by bad traffic, while allowing good traffic through, keeping websites, applications and APIs highly available and performant.

### HTTP Flood (Layer 7)

HTTP flood attacks generate high volumes of HTTP, GET, or POST requests from multiple sources, targeting the application layer, causing service degradation or unavailability.

Defend against the largest attacks

### Shared Network Intelligence / Collective Intelligence

With every new property, contributor and person using this script your help and contributions to this script makes everyones network safer. You are helping identify and block new and evolving threats across the entire internet back bone / infrastructure.

### No Performance Tradeoffs

Eliminate security induced latencies by integrating my script with your servers. You do not need to rely on third party services like Cloudflare, BitMitigate, Sucuri or other such CDN Cloud distributed networks or companies anymore I have given you the tool for free.

### Web Application Firewall

Enterprise-class web application firewall (WAF) protects your Internet property from common vulnerabilities like SQL injection attacks, cross-site scripting, and cross-site forgery requests and protectects your existing infrastructure.

### Rate Limiting

Control to block suspicious visitors.

Rate Limiting protects against denial-of-service attacks, brute-force login attempts, and other types of abusive behavior targeting the application layer.

Rate Limiting provides the ability to configure thresholds, define responses, and gain valuable insights into specific URLs of websites, applications, or API endpoints. It adds granular HTTP/HTTPS traffic control. This also reduces bandwidth costs by eliminating unpredictable traffic spikes or attacks.

## Protect any Web Application

This script can protect every web application ever built.

- WordPress / Joomla / Drupal / Plone / ...
- Magento / Shopify / WHMCS / OpenCart / Prestashop / ...
- Atlassian / GitLab / ...
- PHP/ Symfony / Python / scripts
- Social networks
- Gaming networks servers sites
- Forums / vBulletin / phpBB / MyBB / Simple Machines Forum / XenForo
- Any web hosting
- Backends proxy proxies
- And much more...

## Tor network / Project .onion

You can also use this script to protect servers and sites on the Tor network preventing ddos on .onion links. It can help stop attacks on the deepweb / darkweb aswell as on the mainline internet for those who browse your site through the tor browser it makes sure they are legitimate users.

## HTTP(S) / HTTP2 / HTTP3 / QUIC

So with modern internet protocols yes this script does work with all of them! It can protect both encrypted and unencrypted connections and traffic served over TCP aswell as UDP the new method for HTTP3/QUIC connections.

## Works with

- Nginx + Lua
- OpenTesty
- Custom Nginx builds with Lua compiled
- Litespeed / Litespeedtech as [can be seen here](https://openlitespeed.org/kb/openlitespeed-lua-module/), the reason this works with Litespeed Lua is because they use Openresty Lua builds on their server as [can be understood here](https://openlitespeed.org/kb/openlitespeed-lua-module/#Use)
