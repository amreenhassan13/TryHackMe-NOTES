# TryHackMe - Offensive Security Intro

This room introduces the basics of offensive security by using **Gobuster** to discover hidden web pages on a fake banking website.

---

## 🧠 Objective

Use Gobuster to brute-force the FakeBank website (`http://fakebank.thm`) and discover hidden directories or admin panels.

---

## 🛠 Tool Used: Gobuster

Gobuster is a command-line tool used to brute-force:

* URIs (directories and files) in web sites
* DNS subdomains
* Virtual hosts

In this room, we use Gobuster in **directory scanning** mode.

---

## 💻 Command Used

```bash
gobuster -u http://fakebank.thm -w wordlist.txt dir
```
## 🪜 Steps Followed

- Opened a terminal (command-line interface).
- Ran Gobuster to enumerate hidden pages on the target.
- Identified potentially sensitive directories (e.g., `/admin`).
- Learned how attackers find misconfigured or exposed web areas.
