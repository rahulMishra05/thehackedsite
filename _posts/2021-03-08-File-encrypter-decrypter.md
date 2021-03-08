---
layout: post
title: "File Encrypyter and Decrypter"
date:   2021-03-08 17:26:50 +0530
categories: Shell Script
---
**In this article I am going to show you how to make a command line tool that will encrypt a file or decrypt a file. This command line tool is going to be a shell script.**

*Before diving into the development phase let’s clear some concepts and terminologies.*

**What is encryption?**\
Encryption is a way of scrambling data so that only authorized parties can understand the information. In technical terms, it is the process of converting human-readable plaintext to incomprehensible text, also known as ciphertext. In simple terms, encryption takes readable data and alters it so that it appears random. Encryption requires the use of a cryptographic key. It is a set of mathematical values that both the sender and the recipient of an encrypted message agree on.

**What is decryption?**\
The conversion of encrypted data into its original form is called decryption. It is generally a reverse process of encryption. It decodes the encrypted information so that an authorized user can only decrypt the data because decryption requires a secret key or password.

Now that you have a basic understanding of encryption and decryption, the image of this project is becoming clear, but now you want to know that how will we do this. So for that we will be using GPG, and you will be thinking that what this **GPG** is.
GPG or GnuPG, stands for GNU Privacy Guard. GPG is a different implementation of the open PGP standard and a strong alternative to Symantec’s official PGP software.\
GPG is defined by RFC 4880 *(the official name for the Open GPG standard.)* The GPG project provides the tools and libraries to allow users to integrate encryption with emails and operating systems like Linux. GPG can open and decrypt files encrypted by PGP or open PGP, meaning it works well with other products.

*Enough theory let’s start coding our file encrypter and decrypter.*\
1. Step one make a shell script file using touch command and give whatever name you want to give it. I am giving it [encrypt.sh](https://github.com/rahulMishra05/file_encrypter_decrypter/blob/main/encrypt.sh)
    ```shell
    touch encrypt.sh
    ```
2. Make sure to make changes in the file permissions so that you can execute this shell script file, you can do it like this 
    ```shell
    chmod 744 encrypt.sh
    ```
3. Now start coding the script. First prompt a message to the user and ask what they want to do encrypt or decrypt. 
    ```shell
    echo "File encrypter/decrypter"

    echo "Please select what you want to do"

    choise="Encrypt Decrypt"
    ```
4. Then we will use a select statement and make a decision on the basic of input
    ```shell
    select option in $choise; 
    do
        # Code will come here
    done
    ```
5. Then use if-else statement and perform encryption or decryption.
6. If user entered 1 than write the logic of encrypting a file, if user enter 2 than write the logic to decrypt the file and if the user enter something other than this, that prompt an error. 
So the code for it will be like this.
    
    ```shell
    if [ $REPLY = 1 ];
    then 
	    echo "You have selected Encryption"
	    echo "Please enter the name of the file (including extension)"
	    read file;
	    gpg -c $file
	    echo "File is encrypted"
	    break

    elif [ $REPLY = 2 ]
    then 
	    echo "You have selected Decryption"
	    echo "Please enter the name of the file (including extension)"
	    read file2;
	    gpg -d $file2
	    echo "File is decrypted"
	    break

    else
	    echo "You have selected invalid option"
    fi
    ```

The code for file encryption and decryption completed. You can also see the complete code [here](https://github.com/rahulMishra05/file_encrypter_decrypter)

*So this was all about file encrypter and decrypter. Hope you liked it and learned something new from it.*

**If you have any doubt, question, quires related to this article or just want to share something with me, than please feel free to contact me.**

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