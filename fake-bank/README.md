# Fake Bank - TryHackMe Walkthrough

## Objective
Explore and Exploit a vulnerable web application(in this case, Fake Bank) using Gobuster to brute-force the website and gain information on unsecured pages.

## Steps Taken

### 1. Directory Enumeration with Gobuster
I ran Gobuster to discover hidden directories in the Fake Bank's server.

```bash
gobuster -u http://fakebank.thm -w wordlist.txt dir
```
The scan revealed 2 directories.

<img width="300" alt="Screenshot 2025-06-09 at 1 33 45 PM" src="https://github.com/user-attachments/assets/31f7208f-3b12-4426-993d-d4b7fbe6676c" />

### 2. Navigate to the hidden directory page
I navigated to the /bank-transfer page and found a form to transfer payments.

<img width="300" alt="Screenshot 2025-06-09 at 1 35 14 PM" src="https://github.com/user-attachments/assets/49c3d09c-633c-467e-b8a5-e2007310cce3" />
<img width="300" alt="Screenshot 2025-06-09 at 1 35 06 PM" src="https://github.com/user-attachments/assets/9cd13fd3-8d20-4f71-b7b6-99dbaae5d0c6" />

(All Account Numbers are fake in this exercise, so I did not hide them.)

### 3. Test to ensure results
I successfully transferred the money into my account.

<img width="300" alt="Screenshot 2025-06-09 at 1 35 42 PM" src="https://github.com/user-attachments/assets/08d9bf9e-50d8-4c08-b92d-c6c0f0576bc8" />

## Conclusion
This room was a valuable exercise in discovering exploits in hidden web directories. I was able to practice Gobuster and learned how to use it to find these hidden directories.

### Lessons Learned
- How to use Gobuster for directory discovery
- Identifying and exploiting file transfer vulnerabilities in web applications
- The importance of verifying each step through practical tests.
