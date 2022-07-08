<h3>Natas:level 0</h3>
<p>
	First level you just have to click on this <a href="http://natas0.natas.labs.overthewire.org">link</a> and connect using natas0:natas0.
You then have to inspect the page to find the password for the next level.
</p>

<h3>Natas:level 1</h3>
<p>
	First, you just have to click on this <a href="http://natas0.natas.labs.overthewire.org">link</a> and connect using natas0:natas0.
You then have to inspect the page to find the password for the next level.
</p>

<h3>Natas:level 2</h3>
<p>
	First level you just have to click on this <a href="http://natas0.natas.labs.overthewire.org">link</a> and connect using natas2:pwd.
You then have to inspect the page to find find there is an image : pixel.png stored in a folder files, when we access files by adding /files in the url we can see there is another files called users.txt where the password for the next level is stored.
</p>


<h3>Natas:level 3</h3>
<p>
	First, you just have to click on this <a href="http://natas3.natas.labs.overthewire.org">link</a> and connect using natas3:pw.
Google uses web-crawlers / web-spiders robots to run around every website and read its content.
To display hidden folders that can't be accessed by web crawlers, check the robots.txt file in the server.
The robots text file shows that there is a directory called "S3cr3t" in the server, that has the file users.txt with the pw for the next level.
<!--One tool to catch the files and directories using the website url,  through brute force : dirbuster.-->
</p>

<h3>Natas:level 4</h3>
<p>
	First, you just have to click on this <a href="http://natas4.natas.labs.overthewire.org">link</a> and connect using natas4:pw.
	you can see a message saying: "Access disallowed. You are visiting from "" while authorized users should come only from "http://natas5.natas.labs.overthewire.org/"", to get access you have to change the referrer to natas5 url, to do so you can add a line in burp's proxy request:
	Referer: http://natas5.natas.labs.overthewire.org/, you then get redirected to a page with a password for the next level

</p>

<h3>Natas:level 5</h3>
<p>
	First, you just have to click on this <a href="http://natas5.natas.labs.overthewire.org">link</a> and connect using natas5:pw.
	You can see a message saying :"Access disallowed. You are not logged in", after just logging in, but if you search in cookies, you'll find the value of loggedin set to 0. After setting it to 1 and reloading the page we get the password for the next level.

</p>

<h3>Natas:level 6</h3>
<p>
	First, you just have to click on this <a href="http://natas6.natas.labs.overthewire.org">link</a> and connect using natas6:pw.
	We can see that there is a textbox where you appareently have to paste in the secret code to get the pw for the next level, and a link to the source code of that page. We need the source code beecause we can't see php code from console because it's only stored on the server unlike the html and css code that you can freely navigate. 
In this source code written in php, we see an a file included : "includes/secret.inc" so now we just have to copy paste in with the rest of the url and you'll have to secret code.

</p>

<h3>Natas:level 7</h3>
<p>
	First, you just have to click on this <a href="http://natas6.natas.labs.overthewire.org">link</a> and connect using natas6:pw.
	We can see that there is a textbox where you appareently have to paste in the secret code to get the pw for the next level, and a link to the source code of that page. We need the source code beecause we can't see php code from console because it's only stored on the server unlike the html and css code that you can freely navigate. 
In this source code written in php, we see an a file included : "includes/secret.inc" so now we just have to copy paste in with the rest of the url and you'll have to secret code.

</p>

<h3>Natas:level 8</h3>
<p>
	First, you just have to click on this <a href="http://natas8.natas.labs.overthewire.org">link</a>
	Once we click on the page source link in the page, we notice that the php code encodes the secret password using: bin2hex, strrev, base64_encode.
	All we haveto do is decode the secret using hex2bin, strrev, base64_decode to get the right password 

</p>
	
<h3>Natas:level 9</h3>
<p>
	First, you just have to click on this <a href="http://natas9.natas.labs.overthewire.org">link</a>
	input given by the user is executed automatically in the function passthru, all we have to do is inject a command to get to the content of /etc/natas_webpass/natas10 by using "; cat /etc/natas_webpass/natas10"
(path traversal; command injection)
</p>
	
<h3>Natas:level 10</h3>
<p>
	First, you just have to click on this <a href="http://natas10.natas.labs.overthewire.org">link</a>
	Now there is a the input filtering is more secured and we can use characters such as "; | &" to inject a second command withing the code, but we can still use grep since we know where the password is.
The command normally executed is : "grep -i $key dictionary.txt", we can use grep to get the first line from the file we want using this command: "-m1 "" /etc/natas_webpass/natas11" we then get the output we need
</p>

