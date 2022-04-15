# SQL-injection-attack
Sql injection using basic tricks to gain admin login


</br>
</br>

Cn mini project

Our aim is to protect our login page against SQL injections.
We have two sections in our mini-project.
1.	Shows how that web page is vulnerable 
2.	How we can prevent it from happening

1.	How to know if the website is vulnerable to SQL injections?
<br>
![Picture1](https://user-images.githubusercontent.com/100014146/163600614-59334037-d69d-4039-9d6a-17fc6a98463a.png)
 
 <br>
 

When the user enters the correct user name and password, he is shown the login page.

<br>
 
![Picture2](https://user-images.githubusercontent.com/100014146/163600705-6b90ab6f-2fbb-4015-970a-c32cbfdb1652.png)

<br>

Or else he is shown Invalid user title.
 <br>
 ![Picture3](https://user-images.githubusercontent.com/100014146/163600787-1aa98625-f92e-4df9-9960-66b9283cf32b.png)
</br>

This is for the normal user. When an attacker visits our website and enters a malicious code to it like ‘  in the user name or password we get this error.
 <br>
 
![Picture4](https://user-images.githubusercontent.com/100014146/163600848-ede3ea31-679f-4a87-8e31-3ef7bd3ac1b8.png)

<br>

This tells the attacker that there is some kind of error In the system.
Digging deep into it on entering 1' or '1' = '1
 
 <br>
 
 ![Picture5](https://user-images.githubusercontent.com/100014146/163600932-195e0564-6c7f-4e26-9aa6-b2a4b518040b.png)
 
 <br>
![Picture6](https://user-images.githubusercontent.com/100014146/163601017-829c11f9-85ca-4f61-9e5c-408eff443baf.png)

When the attackers enter into the database and perform SQL injection, He gets logged in to the system and gets the rights of the first person in the database which is the ADMIN.

Securing webpage
Thus, we have developed a system in which if the enters miscellaneous letters in the text field, it gets a vulnerability level number. And when that number crosses 10, the user is given an unauthorized error message.
If an attacker enters ‘ = the vulnerability level increases by 10 and so do others
 ![Picture7](https://user-images.githubusercontent.com/100014146/163601070-943200ea-b62f-4eb9-9a24-b7b51ea380ce.png)


And when user enters; it increases by 9
 ![Picture8](https://user-images.githubusercontent.com/100014146/163601115-a1effb1b-9234-4e2e-87c1-97de98d3d881.png)

To take the security to another level, we have also taken care of advanced keywords used in MySQL.
SQLI_INJECTION_KEYWORDS.txt
Contains all the important keywords possible which can be probably used for hacking
We use explode method which converts words having spaces in between into variable names on which we can assign values later. But the best part about exploding is in case we don’t assign values to the variables formed from the txt file, then It holds the name of the variable itself. Thus technically we converted the txt file and converted to a separate word.

 ![Picture9](https://user-images.githubusercontent.com/100014146/163601152-d57c1ebb-2def-4f7f-bd1b-1b2524afe631.png)

Now whenever  the attacker enters  commands from the above text files the vulnerability_level variable increases by 2 for each keyword 

And when that vulnerability level becomes greater than 10, the user which is potentially an attacker gets an unauthorized error.
 
![Picture10](https://user-images.githubusercontent.com/100014146/163601182-ce42d036-9c31-481a-834f-8400daa35209.png)


