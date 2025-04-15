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
  3. Found tweet with [full name](screenshots/fullname.png)
- **Answer:** `Aiko Abe`

## Task 4 - UNVEIL

### Q1: What cryptocurrency does the attacker own a cryptocurrency wallet for?
- **Method:**  
  Found `ETH` repo in SakuraSnowAngelAiko's GitHub → Clear   [Ethereum reference](screenshots/etherium.png)
- **Answer:** `Ethereum`  

### Q2: What is the attacker's cryptocurrency wallet address?
- **Method:**
  1. Reviewed commit history in [ETH](screenshots/walletaddress1.png) repo
  2. Found address in Commit [5d83f7b](screenshots/walletaddress2.png)
- **Answer:** `0xa102397dbeeBeFD8cD2F73A89122fCdB53abB6ef`  

### Q3: What mining pool did the attacker receive payments from on January 23, 2021 UTC?
- **Method:**
  1. Queried address on [Etherscan](https://etherscan.io)
  2. Filtered transactions for `Jan 23, 2021`
  3. Identified mining payout from [pool](screenshots/payment.png)
- **Answer:** `Ethermine`  

### Q4: What other cryptocurrency did the attacker exchange with using their cryptocurrency wallet?
- **Method:**  
  1. Used Etherscan Advanced Filter 
  2. Selected `Asset` tab  
  3. Found USDT (Tether) [transactions](screenshots/othercrypto.png)
- **Answer:** `Tether`  
