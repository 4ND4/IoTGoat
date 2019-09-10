<h3>Challenges</h3>

Examples of vulnerabilities included in IoTGoat consist of the following. Boxes checked are included included in the latest release.

No 1: Weak, Guessable, or Hardcoded Passwords:
Recompile uhttpd and insert hardcoded backdoor user and password that grants admin rights on the web interface.
Add hardcoded encryption key in a network service that uses encryption.

- [x] Hardcoded user credentials compiled into firmware. 

No 2: Insecure Network Services:
- [x] Vulnerable miniupnp configuration allowing unauthorized devices permission to change firewall rules. This attack can be demonstrated using the [Miranda tool](https://tools.kali.org/information-gathering/miranda)

No 3: Insecure Ecosystem Interfaces:
Have an unauthenticated SOAP service that can be used to enumerate system users or perform other privileged actions.

- [x] A "secret" developer diagnostics page that is not directly accessible and exposes shell access to users. 
- [x] Persistent backdoor daemon configured to run during start up. 


No 4: Lack of Secure Update Mechanism:
Install a custom service that emulates an insecure vendor update mechanism - perhaps rely on second VM that will have the role of the vendor cloud where updates will be pulled from

No 5: Use of Insecure or Outdated Components:
Find a public CVE associated with one of the components of OpenWrt and install that vulnerable version on our image.


No 6: Insufficient Privacy Protection:
Install database locally with cleartext sensitive information (PHI / PII) and expose through network - associated vulnerabilities could be a SQL or command injection.

No 7: Insecure Data Transfer:
Http instead of https, cleartext transmission of PII from database, telnet. 

No 8: Lack of Device Management:
configure OpenWrt so that it cannot update packages by default

No 9: Insecure Default Settings:
default user for web interface, make some settings (such as disabling UPnP) not configurable through the web interface

No 10: Lack of Physical Hardening:
This will not be probably included in IoT goat due to limiting the project to software only - no hardware component for now.

No 11: Embedded credentials in internal components:
Embed credentials of another service (could be one of the existing ones) in a compiled Java application (JAR file). Application could be added to the firmware file so users can find it through firmware analysis or another vulnerability such as a local file inclusion.

No 12: Insecure firmware build system:
Develop custom firmware builds of the latest OpenWrt version (18.06) demonstrating the process of incorporating debug services/tools, misconfigurations, and usage of vulnerable software packages.

<h4>Things to consider:</h4>

In what form is the documentation going to be presented? We could start with an OWASP wiki page.
Will every vulnerability be first demonstrated in a step-by-step tutorial and then an additional exercise will have to be completed by the reader?  Or alternatively give the user a high-level description of the challenge and let them do it themselves.
CTF-like flags for each challenge

Challenge ideas and status could be found withint he [project task sheet](https://docs.google.com/spreadsheets/d/1KXX2K7ikkve6wmdfAVu-sZONgKEBuAkRij_paJUgX2w/edit#gid=0)

<h5>Roadmap:</h5>

September 2019: No5 No8\
October 2019: No6\
November 2019: No7 No 9\
December 2019: No4
