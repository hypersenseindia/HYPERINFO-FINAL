# HYPERINFO &mdash; Final

**Terminal OSINT for Termux.** Give it an IP address or hostname and it gathers only what is already public: WHOIS, ASN and ISP, reverse DNS, geolocation, certificate transparency and, optionally, Shodan banners.

**Passive only.** It never scans, probes or touches the target.

## What it collects

| Source | Data |
| --- | --- |
| WHOIS | Registrant organisation, netblock, abuse contact |
| DNS | Reverse lookup, A / MX / NS records |
| crt.sh | Certificate transparency entries, which often expose sibling hostnames |
| Shodan (optional) | Open ports and service banners, if you supply a key |
| Public text | Emails and phone numbers found in the publicly available records |

## Run

```bash
pkg install -y git python whois
git clone https://github.com/hypersenseindia/HYPERINFO-FINAL
cd HYPERINFO-FINAL
bash HYPERINFO_FINAL.sh
```

Run passcode: `321`

## Optional keys

```bash
export SHODAN_API_KEY="..."
```

Without a key, the Shodan stage is skipped and every other lookup still works.

## Editions

This repository is the **final CLI build**. Two other editions exist:

- [HYPERINFO-hypersenseindia](https://github.com/hypersenseindia/HYPERINFO-hypersenseindia) &mdash; the original
- [HYPERINFO-PAGES](https://github.com/hypersenseindia/HYPERINFO-PAGES) &mdash; page-by-page GUI report

## Legal

Passive collection of public records only. Do not use it to harass, stalk or identify private individuals. Active scanning of systems you do not own may be illegal where you live.
---

<p align="center">
  <sub>Built by <b>AG HYDRAXFF</b> &mdash; HYPERSENSEGLOBAL &middot;
  <a href="https://www.instagram.com/hydraxff_yt/">@hydraxff_yt</a></sub>
</p>