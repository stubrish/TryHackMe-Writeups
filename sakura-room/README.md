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

## Task 5 - TAUNT

### Q1: What is the attacker's current Twitter handle?
- **Method:**
    Checked Twitter/X: via Google: `sakurasnowangelaiko `
- **Answer:** `SakuraLoverAiko`

### Q2: What is the BSSID for the attacker's Home WiFi? 
- **Method:**
  1. All the hints given in the Twitter/X i tried but the deep paste onion site was not working hence used the image provided by the room maker and found the Home [WIFI name](screenshots/darkweb.png)
  2. Searched network name `DK1F-G` on [Wigle](https://wigle.net/) → Found [BSSID](screenshots/wigle.png)
- **Answer:** `84:af:ec:34:fc:f8`

## Task 6 - HOMEBOUND

### Q1: What airport is closest to the location the attacker shared a photo from prior to getting on their flight?
- **Method:**  
  1. Found a picture with the a tweet saying -> Checking out some last minute cherry blossoms before heading home!
  2. After a through analysis found out the airport by searching for the [monument](screenshots/twitterpic.png) in the picture
  3. Searched for the [airport](https://www.nationsonline.org/oneworld/IATA_Codes/airport_code_list.htm) and found out the code [airport code](screenshots/airportcode.png)
- **Answer:** `DCA`  

### Q2: What airport did the attacker have their last layover in?
- **Method:**  
  1. Found a picture with the a tweet saying -> My final layover, time to relax!
  2. After a through analysis and searching for first class loung i found out the [answer](screenshots/lounge.png)
- **Answer:** `HND`  

### Q3: What lake can be seen in the map shared by the attacker as they were on their final flight home?
- **Method:**  
  1. Found a picture with the a tweet saying -> Sooo close to home! Can't wait to finally be back! :)
  2. After a through analysis and searching for the lake i [got](screenshots/lake.png)
- **Answer:** `Lake Inawashiro`  

### Q4: What city does the attacker likely consider "home"?
- **Method:**  
  Well for this question as we already had the picture from the darkweb there is the city name in that [picture](screenshots/darkweb.png)  or we can just do a through analysis from the information obtained throughout the Lab.
- **Answer:** `Hirosaki`  
