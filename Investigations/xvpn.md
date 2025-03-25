# Investigation on X-VPN
Collected by Andrew Robinson
Verdict: Evasive, ignores antivirus, identification stealer

Malware: Possibly
Dangerous: YES
Should be disabled: YES

Summary:
- The reason why X-VPN works is that it sends an invalid payload of a website that is not true; this evades antivirus
- Uses homegrown protocols which are possibly insecure

Flags:
- Spoofs normally allowed URLs such as google.com and bing.com [SEVERE FLAG + BREACH OF DOMAIN PRIVACY POLICY]
- Collects a large amount of user data [RED FLAG]
- Uses unidentified protocols [SEVERE FLAG]
- Based in Hong Kong (HK) [RED FLAG]
- Misinformation on the website [SEVERE FLAG]
- Plagiarism on the website's privacy policy (copies ExpressVPN) [ILLEGAL]
- X-VPN uses
    Your email address [FINE]
    Connection timestamps [FINE]
    Protocol used [SEVERE]
    Network type [SEVERE]
    Error reports (analytics) [FINE]
    Device information
    App version [FINE]
    Data usage [FINE]
    Geolocation (city) [SEVERE]
    Payment data [SEVERE + ILLEGAL]
    Originating IP address when signing in to the website [SEVERE]
    [SEVERE FLAG] (IDENTIFICATION STEALER)
- Self-developed protocols that are confidential? [SEVERE FLAG] (F.Y.I: X-VPN uses its own protocols that could easily be stolen)
- Bogus stats: https://cdn.comparitech.com/wp-content/uploads/2021/03/VPN_Protocols2.jpg [RED FLAG]
- DNS Leaks present; is not a VPN [SEVERE FLAG]
- Possible chain of third-party VPN [SEVERE FLAG]
- $5.99/mnth; actual scam [RED FLAG]
- It does use (some) well known protocols such as FastLemon VPN protocol [NO ISSUE]


References:
- https://unit42.paloaltonetworks.com/evasion-of-security-policies-by-vpn-clients-poses-great-risk-to-network-operators/
- https://www.comparitech.com/vpn/reviews/xvpn-review/
- https://www.fortiguard.com/appcontrol/43539

## Solution
Disable this application in MDAC or Forti.
