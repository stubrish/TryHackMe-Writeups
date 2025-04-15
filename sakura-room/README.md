#  Sakura Room (OSINT) Writeup  

**Completed:** 16-04-25 
**Difficulty:**  Easy 
 

---

##  Walkthrough

## Task 1 - Introduction
**Question:** Are you ready to begin?
- **Objective:** Read the briefing 
- **Answer:** `Let's Go!` 

## Task 2 - TIP-OFF
**Question:** What username does the attacker go by?
- **Objective:** Find attacker's username from image metadata
- **Method:**
  1. Open the provided image
  2. Viewed source code (Right Click → View Page Source)
  3.  Found username in source code → [Here](screenshots/tip-off.png)
- **Answer:** `SakuraSnowAngelAiko`

## Task 3 - RECONNAISSANCE

### Question 1: What is the full email address used by the attacker?
- **Method:**
  1. Checked Github via Google: `"SakuraSnowAngelAiko"`
  2. Located `PGP` repo → found [publickey](screenshots/PGP.png) file
  3. Found email in decoded PGP key:  
  [CyberChef output](screenshots/cyberchef.png)
- **Answer:** `SakuraSnowAngel83@protonmail.com`

### Question 2: What is the attacker's full real name?
- **Method:**
  1. Checked Twitter/X: via Google: `SakuraSnowAngelAiko `
  2. Profile revealed: `@SakuraLoverAiko`
  3. Found tweet with [full name](screenshots/twitter_reveal.png)
- **Answer:** `Aiko Abe`
