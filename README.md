# SSH-Password-Cracking
Explore powerful tools and scripts for cracking SSH passwords, uncovering weak configurations, and enhancing security. Test and strengthen your defenses against potential vulnerabilities with brute force attacks and dictionary-based cracking techniques.


Contents:
1) Hydra
2) Medusa
3) Metasploit
4) Ncrack


**<h1>Hydra</h1>**

   Hydra is a versatile and powerful password cracking tool that supports various protocols, including SSH, HTTP, FTP, and more. With its advanced capabilities and extensive options, Hydra enables efficient and targeted password guessing attacks, helping to identify weak credentials and enhance security measures.

   ```hydra -L username.txt -P password.txt 192.168.0.1 ssh```
   The command hydra -L username.txt -P password.txt 192.168.0.1 ssh is used to initiate a brute-force password cracking attack on an SSH (Secure Shell) server located at the IP address 192.168.0.1.

Here's a breakdown of the command:

    1) hydra: Refers to the Hydra tool itself, which is a popular and powerful network login cracker.
    2) -L username.txt: Specifies the file username.txt containing a list of usernames to try during the password cracking attempt.
    3) -P password.txt: Specifies the file password.txt containing a list of passwords to try during the cracking attempt.
    4) 192.168.0.1: Represents the IP address of the target SSH server.
    5) ssh: Indicates that the cracking attempt is focused on the SSH protocol.

By providing the tool with a list of usernames and passwords, Hydra systematically attempts to log in to the SSH server using different combinations until it finds a successful match or exhausts all possibilities. This command can be used for security testing purposes to identify weak or easily guessable credentials on SSH servers.



**<h1>Medusa</h1>**

Medusa is a command-line network login brute-forcing tool used to test the security of various network services. With its flexible and powerful capabilities, Medusa can perform brute-force attacks on protocols such as SSH, Telnet, FTP, HTTP, and more. It supports various authentication methods and allows for the customization of attack parameters, including username and password lists. Medusa is an efficient tool for security professionals and penetration testers to identify weak credentials and vulnerabilities in network services.

```medusa -h 192.168.0.1 -U username.txt -P password.txt -M ssh```


The command you provided is an example of how to use Medusa, a network login brute-forcing tool, to perform a specific task.

    1) -h 192.168.0.1: Specifies the target host IP address.
    2) -U username.txt: Specifies the file containing a list of usernames to use in the brute-force attack.
    3) -P password.txt: Specifies the file containing a list of passwords to use in the brute-force attack.
    4) -M ssh: Specifies the module to be used for the attack, in this case, SSH.

By executing this command, Medusa will attempt to brute-force the SSH service on the target host using the provided username and password lists. It systematically tries different combinations until it finds a successful login or exhausts all the possibilities. This tool helps assess the security of SSH by identifying weak credentials and potential vulnerabilities in the authentication process.


**<h1>Metasploit</h1>**

Metasploit SSH Cracker is a powerful tool within the Metasploit Framework that enables penetration testers and security professionals to perform brute-force attacks against SSH (Secure Shell) services. With its extensive collection of pre-defined usernames and password combinations, it automates the process of attempting various credentials to gain unauthorized access to SSH servers. This tool helps identify weak authentication mechanisms, allowing organizations to strengthen their SSH security and protect against potential unauthorized access.

```use auxiliary/scanner/ssh/ssh_login
set rhosts 192.168.0.1
set user_file username.txt
set pass_file password.txt
run
```

The provided commands are specific to the usage of the Metasploit Framework, which is a powerful open-source tool for penetration testing and vulnerability assessment. Let's break down the commands:

    set rhosts 192.168.0.8: This command sets the target host IP address to 192.168.0.8. It specifies the remote host that the Metasploit module will target for the operation.

    set user_file user.txt: This command sets the file containing a list of usernames to be used during the SSH password cracking process. The usernames will be read from the "user.txt" file.

    set pass_file password.txt: This command sets the file containing a list of passwords to be used during the SSH password cracking process. The passwords will be read from the "password.txt" file.

    run: This command initiates the execution of the module with the specified parameters. It starts the process of attempting to crack SSH passwords using the provided username and password lists against the specified target host.

Overall, these commands configure the necessary parameters for the Metasploit module to perform a brute-force attack on SSH services, attempting various combinations of usernames and passwords from the specified files against the target host (192.168.0.8) to gain unauthorized access.


**<h1>Ncrack</h1>**


Ncrack is a powerful network authentication cracking tool designed to assist in assessing the security of network services. It allows security professionals and penetration testers to efficiently and effectively crack passwords and perform brute-force attacks on various protocols such as SSH, RDP, FTP, and more. With its flexible and extensible architecture, Ncrack provides a command-line interface and supports parallelized cracking, making it a valuable tool for assessing the strength of network authentication mechanisms and identifying potential vulnerabilities.

```ncrack -U username.txt -P password.txt 192.168.0.1```


The command ncrack -U username.txt -P password.txt 192.168.0.1 is used to launch a password cracking attack using Ncrack tool. It specifies the target IP address 192.168.0.1 and the username and password files (username.txt and password.txt) containing the list of credentials to be tested. Ncrack will systematically attempt each combination of usernames and passwords to gain unauthorized access to the target system. This command helps assess the strength of authentication mechanisms by identifying weak or easily guessable credentials.
