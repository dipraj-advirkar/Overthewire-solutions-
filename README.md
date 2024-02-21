# Overthewire-solutions
https://overthewire.org/wargames/natas/

Project Name: Overthewire/wargames/natas
=============================================================================================================================================================================
Description
=============================================================================================================================================================================
Natas

Natas teaches the basics of serverside web-security.

Each level of natas consists of its own website located at http://natasX.natas.labs.overthewire.org, where X is the level number. There is no SSH login. To access a level, enter the username for that level (e.g. natas0 for level 0) and its password.

Each level has access to the password of the next level. Your job is to somehow obtain that next password and level up. All passwords are also stored in /etc/natas_webpass/. E.g. the password for natas5 is stored in the file /etc/natas_webpass/natas5 and only readable by natas4 and natas5.


Natas Level 0
============================================================================================
Start here:

Username: natas0
Password: natas0
URL:      http://natas0.natas.labs.overthewire.org

Open 
"http://natas0.natas.labs.overthewire.org" link on new tab. 
You will get a pop-up fill there given credentials & go to inspect.

There you will get commented password for natas1:

<!--The password for natas1 is g9D9cREhslqBKtcA2uocGHPfMZVzeFK6 -->

============================================================================================

Natas Level 0 → Level 1 
=============================================================================================================================================================================
Username: natas1
URL:      http://natas1.natas.labs.overthewire.org


It will show you
"You can find the password for the
next level on this page, but rightclicking has been blocked!" But you right click out side of that box
then you can use right click & inspect.

Also you can use shortcut key that's "cntrl + shift + c" to view source code.

And this is how you will get password for natas2.

<!--The password for natas2 is h4ubbcXrWqsTo7GGnnUMLppXbOogfBZ7 -->

============================================================================================


Natas Level 1 → Level 2
=============================================================================================================================================================================
Username: natas2
URL:      http://natas2.natas.labs.overthewire.org

Once you enter password you will get new challenge.

Again Inspect and review code. You will find something intersting like "<img src="files/pixel.png">".

Good!

Now search "/files/" directory after url.

Here, you will get "users.txt".
Open it there you will get natas3 password.

"natas3:G6ctbMJ5Nb4cbFwhpMPSvxGHhQ7I6W8Q"

============================================================================================

Natas Level 2 → Level 3
=============================================================================================================================================================================
Username: natas3
URL:      http://natas3.natas.labs.overthewire.org

After entering credentials.
Inspect the page and view source code. There you will get one hint.
You will find hint. In commented form.

"<!-- No more information leaks!! Not even Google will find it this time... -->"

They are saying not even google will find it this times means:
Some are hidden directories are present there.
So, search for "/robots.txt" file after a url.

There you will get "/s3cr3t/" directory. Search for it.

After searching you will get "users.txt" file Open it you will get password natas4.

"natas4:tKOcJIbzM4lTs8hbCmzn5Zr4434fGZQm"

============================================================================================

Natas Level 3 → Level 4
=============================================================================================================================================================================
Username: natas4
URL:      http://natas4.natas.labs.overthewire.org

After entering credential. You will get new challege.
In which you have to intercpet request using burp-suite.
And change referer this:
Referer:
http://natas4.natas.labs.overthewire.org/index.php

to this:
Referer: http://natas5.natas.labs.overthewire.org/

And forward that request you will get password of natas5:

Access granted. The password for natas5 is Z0NsrtIkJoKALBCLi5eqFfcRN82Au2oD 

============================================================================================

Natas Level 4 → Level 5
=============================================================================================================================================================================
Username: natas5
URL:      http://natas5.natas.labs.overthewire.org


After entering credential. You will get new challege.
In which you have to intercpet request using burp-suite.


And make change in Cookie:

Cookie: _ga_RD0K2239G0=GS1.1.1708541020.3.1.1708541021.0.0.0; _ga=GA1.1.1878625325.1708462980; loggedin=0

In which we have to change boolean value false to true in binary.

In binary is 0 means false and 1 means true.

Cookie: _ga_RD0K2239G0=GS1.1.1708541020.3.1.1708541021.0.0.0; _ga=GA1.1.1878625325.1708462980; loggedin=1

After forwarding this request you will get password of natas6 as

 Access granted. The password for natas6 is fOIvE0MDtPTgRhqmmvvAOt2EfXR6uQgR

=============================================================================================================================================================================

Coming Soon....
Happy Hacking :)



