---
layout: post
title: "Broken Authentication: Methodology & Prevention"
date:   2021-05-12 22:05:05 +0530
categories: Bug Bounty
---
**In this article we will see that how hacker/penetration testers can exploit broken authentication vulnerability, in the authentication system of a website. In the end we will also see some ways by which you can prevent issues related to authentication of your website.**

*Before we discuss about ways in which a hacker/penetration tester can exploit broken authentication vulnerability, we must know the answer of these two questions.*

### 💡 What is broken authentication?
Authentication is broken when attackers are able to compromise passwords, keys or session tokens, user account information, and other details to assume user identities. Due to weakness in design and implementation of identity and access controls, the prevalence of broken authentication is widespread.

### ☠️ What is the impact of broken authentication?
In summary, broken authentication and session management has the potential to steal a user login data, or forge session data, such as cookies, to gain unauthorized access to websites. However, there are clear and easy solutions to prevent your site from being affected by this vulnerability.

Now let’s discuss the way a hacker/penetration tester can exploit this vulnerability.

1. <u>**Credential stuffing attack:**</u> 
    - An attack where the attacker uses lists of compromised credentials to breach a system.
    - Typically uses a bot to automate this process.
    - Has success rate around 0.1%.

    <!-- Image 1 will come here -->
![image1.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1620836802294/QabPRIhAot.png)

2. <u>**Brute force and weak passwords:**</u> 
    - Brute force involves trying common passwords or random combinations to login.
    - Take advantage of weak passwords.
    - Works best on services that do not limit login attempts. 

     <!-- Image 2 will come here -->
![image2.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1620836818937/qduhygZgM.png)

3. <u>**Weak credential recovery:**</u> 
    - When a user forgot their password, they may need to recover it.
    - Password recovery should only work for the user who owned the account.
    - Methods such as recovery questions can be easily guessed, if the hacker/penetration tester knows the person or had done a very good reconnaissance on the target user.

    <!-- Image 3 will come here -->
![image3.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1620836834664/m86de_ZPm.jpeg)

4. <u>**Missing multi-factor authentication:**</u>
    - Multi-factor authentication can help add a layer of security to authentication.
    - Options such as biometrics, phone and e-mail based authentication are good options.
    - Missing multi-factor authentication makes brute force and credential stuffing more effective.

    <!-- Image 4 will come here -->
![image4.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1620836848969/JWR2UQ0VK.png)

5. <u>**Exposed session ID:**</u>
    - If a session ID is exposed through URL or cookies, it can be used by an attacker to authenticate.
    - Session IDs should be properly handles, ideally only on the server side.

    <!-- Image 5 will come here -->
![image5.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1620836877978/BTcUH-mIG.jpeg)

So far we have discussed most common ways to exploit broken authentication vulnerability, now it’s time to see some safety measures to prevent this vulnerability.
- Implement some form of multi-factor authentication.
- Use a password policy to prevent weak logins.
- Do not ship with default credentials, such as `admin:admin` or `root:password`
- Limit failed login attempts.
- Keep session IDs on server side.

    <!-- Image 6 will come here -->
![image6.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1620836953757/Xt0h-ykC7.jpeg)

*So this was all about methodology and prevention of broken authentication vulnerability. I hope you liked it and learned something new from it.*

If you have any doubt, question, quires related to this topic or just want to share something with me, than please feel free to contact me. 

### 🖥 My other blogs
[Dev.to](https://dev.to/rahulmishra05),
[Hashnode](https://hashnode.com/@programmingport)

### 📱 Contact Me

[Twitter](https://twitter.com/r_mishra10),
[LinkedIn](https://www.linkedin.com/in/rahul-mishra-66210b185),
[Telegram](https://t.me/rahul_mishra10),
[Instagram](https://www.instagram.com/rahul_mishra10/?hl=en),

### 📧 Write a mail
<rahulmishra102000@gmail.com>

#### 🚀 Other links

[GitHub](https://github.com/rahulMishra05),
[HackerRank](https://www.hackerrank.com/rahulmishra10201),
[Tryhackme](https://tryhackme.com/p/rahulMishra05)