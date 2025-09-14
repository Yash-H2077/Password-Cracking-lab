# Password-Cracking-lab
This repository contains the implementation of Password Cracking Tools. The objective is to crack password hashes using dictionay and brute force attack by using tools and wordlists in Kali linux 

## Hash types tested
1.MD5  
2.SHA  
3.SHA256


## Tools used:
1.Hashcat  
2.John-the-Ripper  
3.rockyou.txt(wordlist)  


## Create hashes with words 
```bash
# Creating hashes
echo -n "Anyword" | md5sum  # you can replace Anyword with a word of your choice and specify the desired hashing technique
b1a8b7cd2f1eaa474ab6465402e035d2  #this is the new hash code generated 

# saving hashes
echo "b1a8b7cd2f1eaa474ab6465402e035d2" > hash.txt # saves the code into hash.txt file 
```

## Hashcat
Hashcat is a very effective password cracker used by penetration tester as well as cyber criminals. It is used to detect the types of hashing and it also has a lot of attack methods to attack different categories


### Hashcat commands
```bash
# Identifying type of hash
hashid -m "hash.txt"  # identifies the possible hashing techniques used

# Dictionary attack
hashcat -m 0 -a 0 hash.txt /home/yash/Downloads/rockyou.txt  #specify the wordlist directory accordingly
# make sure you specify the mode and attack mode properly before executing (refer the screenshots)
```                                                                                                                                                            
                                                                                                                                                               
                                                                                                                                                               
## John the Ripper                                                                                                                                             
John the Ripper is a open-source password cracking tool which supports multiple platforms and formats, followed by customizable attacks where you can define the rules, formats and wordlists.                                                                                                                                
                                                                                                                                                               
### John-the-Ripper commands                                                                                                                                   
```bash
john --wordlist=rockyou.txt hash.txt --format=raw-md5  #speciy the wordlist directory accordingly 

```
## Screenshots
Refer to the above screenshots and output folders for better explanation 
