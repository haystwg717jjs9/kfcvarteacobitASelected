### A "simple" python application that uses Selenium to help with your M$ Rewards

---

![Static Badge](https://img.shields.io/badge/Made_in-python-violet?style=for-the-badge)
![MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)
![Maintained](https://img.shields.io/badge/Maintained%3F-yes-green.svg?style=for-the-badge)
![GitHub contributors](https://img.shields.io/github/contributors/klept0/MS-Rewards-Farmer?style=for-the-badge)
![GitHub issues](https://img.shields.io/github/issues/klept0/MS-Rewards-Farmer?style=for-the-badge)

---

> [!IMPORTANT]
> If you are multi-accounting and abusing the service for which this is intended - **_DO NOT COMPLAIN ABOUT BANS!!!_**

---

> [!CAUTION]
> Use it at your own risk, M$ may ban your account (and I would not be responsible for it)
>
> Do not run more than one account at a time.
>
> Do not use more than one phone number per 5 accounts.
>
> Do not redeem more than one reward per day.

---

#### Group Chat - [Telegram](https://t.me/klept0_MS_Rewards_Farmer/) (pay attention to captchas - helps prevent spam)

#### Original bot by [@charlesbel](https://github.com/charlesbel) - refactored/updated/maintained by [@klept0](https://github.com/klept0) and a community of volunteers.

#### PULL REQUESTS ARE WELCOME AND APPRECIATED!

---

## Installation

1. Install requirements with the following command :

   `pip install -r requirements.txt`

   Upgrade all required with the following command:
   `pip install --upgrade -r requirements.txt`

2. Make sure you have Chrome installed

3. (Windows Only) Make sure Visual C++ redistributable DLLs are installed

   If they're not, install the current "vc_redist.exe" from this [link](https://learn.microsoft.com/en-GB/cpp/windows/latest-supported-vc-redist?view=msvc-170) and reboot your computer

4. Edit the `accounts.json.sample` with your accounts credentials and rename it by removing `.sample` at the end.

   The "proxy" field is not mandatory, you can omit it if you don't want to use proxy (don't keep it as an empty string, remove the line completely).

   - If you want to add more than one account, the syntax is the following:

   ```json
   [
     {
       "username": "Your Email 1",
       "password": "Your Password 1",
       "proxy": "http://user:pass@host1:port"
     },
     {
       "username": "Your Email 2",
       "password": "Your Password 2",
       "proxy": "http://user:pass@host2:port"
     }
   ]
   ```

5. Run the script:

   `python main.py`

---

## Launch arguments

- -v/--visible to disable headless
- -l/--lang to force a language (ex: en)
- -g/--geo to force a searching geolocation (ex: US)

  `https://trends.google.com/trends/ for proper geolocation abbreviation for your choice. These MUST be uppercase!!!`

- -p/--proxy to add a proxy to the whole program, supports http/https/socks4/socks5 (overrides per-account proxy in accounts.json)

  `(ex: http://user:pass@host:port)`

- -cv/--chromeversion to use a specific version of chrome

  `(ex: 118)`

---

> [!TIP]
> If you are having issues first ask - did I make sure I have updated all of the files and cleared the sessions folder before running again?

> [!TIP]
> Have I tried to run it with -v so I could see what might be causing the error?
---

## Features

- Bing searches (Desktop and Mobile) with current User-Agents
- Complete the daily set automatically
- Complete punch cards automatically
- Complete the others promotions automatically
- Headless Mode - _not recommended at all_
- Multi-Account Management
- Session storing
- 2FA Support
- Notifications via [Apprise](https://github.com/caronc/apprise) - no longer limited to Telegram or Discord
- Proxy Support (3.0) - they need to be **high quality** proxies
- Logs to CSV file for point tracking

---

> [!NOTE]
> You may see [WARNING] in your logs - this is currently enabled for debugging and to provide in any issues you may need to open

## To Do List (When time permits or someone makes a PR)

- [x] Complete "Read To Earn" (30 pts)
- [ ] Setup flags for mobile/desktop search only
- [ ] Setup flags to load config / save data in working directory 
- [ ] Provide Windows Task Scheduler config
