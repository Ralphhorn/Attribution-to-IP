# Attribution to IP
- A collection of methods to learn who the owner of an IP address is.
- The reason for this could be for the IP being victimised in an attack, being currently compromised, or having security misconfigurations and could be attacked.
- These methods are useful for cyber threat intelligence (CTI) analysts performing victim notifications or security researchers working on bug bounty programs. 

## OSINT & Freemium Services
> [!NOTE]
> These are free methods, but paid accounts may be available for some of these services for more information, authenticated APIs, and higher rate limits.

| Method | Description | Source(s) |
| --- | --- | --- |
| Passive DNS (pDNS) | Shows historical DNS resolutions for an IP and allows you to identify domains that have pointed to the IP. | [ViewDNS.info](https://viewdns.info) / [VirusTotal](https://www.virustotal.com)  / [OTX AlienVault](https://otx.alienvault.com/) / [Mnemonic](https://passivedns.mnemonic.no/) / [DNSlytics](https://search.dnslytics.com/) / [subdomainfinder](https://subdomainfinder.c99.nl/) |
| Domain DNS Records | Includes A, PTR, MX, TXT, and CNAME records. PTR records can reveal the hostname; TXT and MX can give clues about the domain’s owner or provider. | [ViewDNS.info](https://viewdns.info) / [CentralOps](https://centralops.net/co/) / [DNSlytics](https://search.dnslytics.com/) / [DNSDumpster](https://dnsdumpster.com/) |
| IP WHOIS | Queries registrar and network block registration info. Can directly identify the entity or ISP that registered the IP range. | [ViewDNS.info](https://viewdns.info) / [DomainTools](https://whois.domaintools.com/) / [CentralOps](https://centralops.net/co/) / [Who.is](https://who.is/) |
| Open Ports & Running Services | Scanning the IP for accessible ports and services. Banner grabbing can reveal software, versions, and sometimes organization names. | [Shodan](https://www.shodan.io/) / [FOFA](https://en.fofa.info/) / [Censys](https://search.censys.io/) / [Onyphe](https://search.onyphe.io/) / [Modat](https://modat.io) / [Odin](https://odin.io/) |
| SSL Certificates | Examine SSL certs served on open HTTPS ports. Certs often contain domains, email addresses, or organization names. | [Certificate Search](https://crt.sh) / [Censys](https://search.censys.io/) / [Modat](https://modat.io) / [Odin](https://odin.io/) |
| Autonomous System Names (ASNs) | ASNs describe ownership of blocks of IP addresses. Helps identify the ISP, hosting provider, or large organization behind a network. | [IPinfo](https://ipinfo.io/) / [InfoByIP](https://www.infobyip.com/) / [IPQS](https://www.ipqualityscore.com/) / [Shodan](https://www.shodan.io/) / [FOFA](https://en.fofa.info/) / [Censys](https://search.censys.io/) / [Onyphe](https://search.onyphe.io/) / [Modat](https://modat.io) / [Odin](https://odin.io/) |
| IP Geolocation | Maps IP to approximate physical location. Helps determine country or city, which may assist in narrowing the scope of who the owner is. | [MaxMind](https://www.maxmind.com/en/geoip-demo) / [IPinfo](https://ipinfo.io/) / [InfoByIP](https://www.infobyip.com/) / [IPQS](https://www.ipqualityscore.com/) / [Shodan](https://www.shodan.io/) / [FOFA](https://en.fofa.info/) / [Censys](https://search.censys.io/) / [Onyphe](https://search.onyphe.io/) / [Odin](https://odin.io/) |
| Border Gateway Protocol (BGP) | BGP announcements tell you who is routing the IP block and confirms the autonomous system or network managing the address. | [BGP Hurricane Electric](https://bgp.he.net/) / [BGP Tools](https://bgp.tools/) |
| Content Archives | Archived content of websites on the IP or screenshots of the services on the IP and may show earlier branding, contact info, or domains before a site changed. | [URLscan](https://urlscan.io/) / [Wayback Machine](https://web.archive.org/) / [Shodan](https://www.shodan.io/) |
| Manual Browsing | Visiting the IP directly in a browser can sometimes reveals landing pages, admin panels, or redirect behavior with company names or logos. | [Browserling](https://www.browserling.com/) |
| Google Dorking | Use advanced search operators to find references to the IP online that could be used to identify its owner. | [Google Dork Examples](https://github.com/BushidoUK/OSINT-SearchOperators/blob/main/GoogleDorks.csv) |
| Code Repositories | Search in code repositories for references to the IP as the developers sometimes hardcode IPs in their code and configuration files. | [GitHub](https://github.com/) / [BitBucket](https://bitbucket.org/) |
| Linked to Tor Nodes, VPNs, or Proxies | Checking in lists of Tor, VPNs, or Proxy nodes suggests the IP is not owned by a specific end-user but part of a privacy or anonymisation network. | [TOR Node List](https://dev.dan.me.uk/tornodes) / [IPQS](https://www.ipqualityscore.com/) / [Spur](https://spur.us/context/me) |
| Cloud Storage | Cloud storage buckets may contain config files, logs, build artifacts, or naming conventions that tie back to the IP owner. | [GrayHatWarfare](https://grayhatwarfare.com/) / [Odin](https://odin.io/) |
| IP Behaviours | Honeypot networks can also help discern what an IP is doing and who owns it based on it's observed interactions with honeypot IPs. | [GreyNoise](https://viz.greynoise.io/) |
| Security TXT Records| Querying the IP directly can reveal the security TXT file at .well_known/security.txt or /security.txt paths on a host ip. DNS implementations also exist for security TXT files, these can be found as DNS TXT records.  | [Browserling](https://www.browserling.com/) /[Mxtoolbox](https://mxtoolbox.com/DNSLookup.aspx) / [urlscan](https://urlscan.io) / [security txt](https://securitytxt.org/) /[dns security txt](https://dnssecuritytxt.org/) |

## Commercial
> [!WARNING]
> These are paid services only typically available for enterprises or public sector organisations and provide more information and authenticated APIs.

| Method | Description | Source(s) |
| --- | --- | --- |
| NetFlow | NetFlow captures metadata about traffic flows (source/destination IPs, ports, protocol, timestamps) and can be used to track communication patterns, peer IPs, and usage behavior. Repeated traffic between an IP and a corporate network could indicate ownership. | [Team Cymru Pure Signal](https://www.team-cymru.com/) |
| Breach Data | Breach Data includes leaked credentials, config files, and service records from compromised systems and could be used to directly connect an IP to an email address, domain, or username and imply corporate ownership. | [SpyCloud](https://spycloud.com/) / [AmIBreached](https://amibreached.com/) |

## Additional Resources
- [Pivot Atlas](https://gopivot.ing/tools/) - A list of various tools and platforms that enable different types of pivots on different types of data.
