# Explore Google hacking and enumeration 

# AIM:

To use Google for gathering information and perform enumeration of targets

## STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various Google hacking keywords and enumeration tools as follows:


### Step 3:
Open terminal and try execute some kali linux commands

## Pen Test Tools Categories:  

| Operator    | Description                        | Example Usage           |
| ----------- | ---------------------------------- | ----------------------- |
| `site:`     | Search within a specific domain    | `site:example.com`      |
| `inurl:`    | Search in URL                      | `inurl:admin`           |
| `intitle:`  | Search in page title               | `intitle:"index of"`    |
| `filetype:` | Search by file type                | `filetype:pdf`          |
| `intext:`   | Search inside page text            | `intext:"confidential"` |
| `link:`     | Pages that link to a specific site | `link:example.com`      |
| `cache:`    | View cached version of a site      | `cache:example.com`     |
| `ext:`      | Same as filetype                   | `ext:xls`               |

 ## Architecture 
 ```
+----------------------+
|   Attacker / Hacker  |
|   (Browser & Google) |
+----------+-----------+
           |
           | Google Dork Queries
           v
+---------------------------+
|       Google Search       |
+---------------------------+
           |
           | Indexed Public Content
           v
+---------------------------+
|   Target Websites / Data  |
| - Leaked files            |
| - Open directories        |
| - Sensitive info          |
+---------------------------+

```


# Output:

# SITE:
<img width="1663" height="1041" alt="site" src="https://github.com/user-attachments/assets/42a939fb-c283-41ff-9780-f526b6124292" />


# INURL:
<img width="1490" height="1032" alt="admin" src="https://github.com/user-attachments/assets/fa4c1ca7-16e0-45f9-86d4-431e3ea43858" />



# INTITLE:

<img width="1571" height="1028" alt="index" src="https://github.com/user-attachments/assets/9563d2c6-f958-4c2f-9f73-3a9b79a1bdc6" />


# FILETYPE:
<img width="1602" height="1044" alt="filetype" src="https://github.com/user-attachments/assets/c82cdb01-1a19-4150-a4af-253ca7c29692" />



# INTEXT
<img width="1425" height="1028" alt="confidentisl" src="https://github.com/user-attachments/assets/0c4c7acc-1b53-4d54-a9cf-e7963da0a1bf" />


# LINK
<img width="1511" height="938" alt="linl" src="https://github.com/user-attachments/assets/564c4611-fcde-4feb-8c89-7120d53a226b" />



# SUBSITES
<img width="1666" height="1038" alt="subsites" src="https://github.com/user-attachments/assets/3636238e-0b9c-4136-892d-7bb7bbd6173d" />





# DNS Enumeration
<img width="653" height="515" alt="image" src="https://github.com/user-attachments/assets/17b63d2b-ff48-459d-a0b7-ee7f2ee43703" />





## DNS Recon

<img width="653" height="515" alt="image" src="https://github.com/user-attachments/assets/3251165d-e59f-47e7-b9ee-a4c0572aad99" />

```
 provides the ability to perform:
 Check all NS records for zone transfers
 Enumerate general DNS records for a given domain (MX, SOA, NS, A, AAAA, SPF , TXT)
 Perform common SRV Record Enumeration
 Top level domain expansion
```



| Record Type | Meaning                        | Example Output                   |
| ----------- | ------------------------------ | -------------------------------- |
| A           | Host to IPv4 address           | `example.com -> 93.184.216.34`   |
| AAAA        | Host to IPv6 address           | `example.com -> ::1`             |
| MX          | Mail server info               | `mail.example.com`               |
| NS          | Name servers                   | `ns1.example.com`                |
| TXT         | Misc data (SPF, verifications) | `v=spf1 include:_spf.google.com` |
| CNAME       | Canonical names (aliases)      | `www -> example.com`             |

## Common Tools Used (Kali Linux)

| Tool           | Description                                | Usage Example                           |
| -------------- | ------------------------------------------ | --------------------------------------- |
| `nslookup`     | DNS lookup tool (simple queries)           | `nslookup example.com`                  |
| `dig`          | DNS lookup utility (detailed)              | `dig example.com any`                   |
| `host`         | Simple DNS querying tool                   | `host example.com`                      |
| `dnsenum`      | Perl script to enumerate DNS info          | `dnsenum example.com`                   |
| `fierce`       | DNS scanner to locate non-contiguous IPs   | `fierce -dns example.com`               |
| `dnsrecon`     | Powerful DNS enumeration script            | `dnsrecon -d example.com -a`            |
| `theHarvester` | Subdomain enumeration using search engines | `theHarvester -d example.com -b google` |


## OUTPUT:

![Uploading image.png…]()



# NSLOOKUP


<img width="651" height="502" alt="image" src="https://github.com/user-attachments/assets/9e9fecef-4f92-454e-9098-add790633f04" />



# DIG

<img width="657" height="513" alt="image" src="https://github.com/user-attachments/assets/38d27fe0-5407-4e1f-9444-a3de7fa2cf98" />



# HOST

<img width="657" height="498" alt="image" src="https://github.com/user-attachments/assets/6c373efa-9732-4e1d-9d10-dac64e434cb6" />




# DNSENUM

<img width="653" height="515" alt="Screenshot 2025-09-13 084923" src="https://github.com/user-attachments/assets/2fe72548-2b95-43d7-bde8-3add10a8dbaa" />



# DNSRECON

![WhatsApp Image 2025-09-05 at 9 16 26 PM](https://github.com/user-attachments/assets/7d150c01-6633-40e7-b630-2e5713b69747)

# FIERCE 
<img width="651" height="501" alt="image" src="https://github.com/user-attachments/assets/33295466-b13b-4730-9fcb-f8153e1d2c4f" />




# Harvestor
![WhatsApp Image 2025-09-05 at 9 16 27 PM (1)](https://github.com/user-attachments/assets/2980881c-e789-4823-81a6-fcbf8907fae5)



## Architecture Diagram 
```
+-------------------+        +------------------+       +------------------+
|                   |        |                  |       |                  |
|   Attacker (You)  +------->|   Target Server   +<----->+    DNS Server    |
| Kali Linux / Parrot|       | (Mail / DNS Host) |       |  (Authoritative) |
+---------+---------+        +---------+--------+       +---------+--------+
          |                            ^                          ^
          |                            |                          |
          |                            |                          |
          |           +-----------------------------+            |
          |           |      Information Tools      |            |
          |           |-----------------------------|            |
          |           | smtp-user-enum              |            |
          |           | nmap --script smtp-enum-*   |            |
          |           | dnsenum                     |<-----------+
          |           +-----------------------------+
          |
          v
+-----------------------------+
|   Output/Report             |
|  - Usernames Found          |
|  - MX Records / Zones       |
|  - Subdomains / IPs         |
+-----------------------------+

```

## dnsenum
**Purpose:** A multithreaded Perl script to enumerate information from DNS servers.

**Use case:** Performs DNS zone transfers, brute force subdomains, and gather host IPs.

```
dnsenum example.com
```

## Output:




## smtp-user-enum
**Purpose:** Standalone tool used to enumerate valid users by using the VRFY, EXPN, or RCPT TO commands.

**Use case:** Brute-forces SMTP to find users.

```
smtp-user-enum -M VRFY -U users.txt -t <target-ip>
```



## nmap –script smtp-enum-users.nse <hostname>

**Purpose:** Uses smtp-enum-users NSE script to enumerate valid users on an SMTP server.

**Use case:** Helps identify email accounts on mail servers.

```
nmap -p 25 --script smtp-enum-users.nse <target-ip>
```
## OUTPUT:

![WhatsApp Image 2025-09-05 at 10 12 10 PM](https://github.com/user-attachments/assets/b20a1957-f5a9-4289-a270-f34bf399c131)




## RESULT:
The Google hacking keywords and enumeration tools were identified and executed successfully
