# Passwords and Passphrases
This page is written with passwords for humans in mind and not service accounts.                                                                                                                                                              
## Good baseline for requirements
 - A minimum of 12 characters
 - Only change passwords if it is believed to be compromised
 - New passwords should be screen against a list of know compromised passwords
 - Do not use password hints or other kinds of knowledge-based security questions
 - Limit the number of failed authentications attempts
 - Allow long passwords
 - Skip character composition rules
 - Allow the use of all printable ASCII characters as well as all UNICODE characters

This was a lot based on the [specopssoft](https://specopssoft.com/blog/nist-password-standards/) list based on NIST.

## Minimum password/passphrases length
Many of the big websites recommend sites with 8 characters as a minimum some websites with even fewer characters. [List from Troy Hunt](https://www.troyhunt.com/how-long-is-long-enough-minimum-password-lengths-by-the-worlds-top-sites/)
NIST in their recommendation also recommends a minimum of 8 characters. Since the recommendation is to not enforce character composition rules 8 characters are a bit low. An 8 character randomized lowercase password can be cracked in
5 hours while a 12 character lowercase will take 2 centuries. Just adding one character increases the complexity a lot. This number is taken from [betterbuys](https://www.betterbuys.com/estimating-password-cracking-times/). With numbers and special characters, it will take a decade. So a solution would be to just enforce special characters?

## Character composition rules
[One tweet to rule them all.](https://twitter.com/brian_bilston/status/1258312717317869568)
Having complex composition rules will make the passwords harder to remember and might backfire and the user chooses a weak password with some letter changes to special characters. The example password is p@ssw0rd. This is still considered a weak password is since permutations like this are easily guessable and therefore does not increase the security.

## Only change compromised passwords
Passwords should only be changed if there are signs that it might be compromised. Having a password rotation policy might in some cases lead to worse security.

The main reason to use password rotation is to reduce the window of opportunity for attackers. If they get a hold of a password it will only be for a limited amount of time before the password is invalid. This only solves the symptom and not the problem. How did the attacker get the password the first time and what stops them from getting the new one? In case of beliving a password has been compromised an investigation on how the password got compromised is needed and change the password when the system is secured.

Being forced to often change the password also hinders users to choose secure passwords. Commonly user only bumps a number at the end of their password by one instead of using a new secure password.

## Screen passwords
All new passwords should be checked against the password list like [Have I Been Pwned](https://haveibeenpwned.com/API/v3#SearchingPwnedPasswordsByRange)                                                                                     
## Password hints and security questions
Password hints should not be used since that can give out information about a password that an attacker can use to figure out the password.                                                                                                  
## Long passwords
Long passwords shall be allowed so that the user can use long generated passwords. There should still be a limit on how long passwords can be. This to protect your system from attackers sending in passwords that are gigabytes in size and perform DOS attack that way.                                                                                                                                                                                                                    
## Allowed characters
All characters should be allowed. Everything from ASCII to special characters and emojis. By allowing all of the characters that are in the Unicode table the number of combinations that attackers we would need to use would increase. As side effect users that come from countries that do not use ASCII by standard, can use their passwords out of the box.                                                                                                                          
## Password manager
Just do it!
