<h3>Natas:level 3</h3>
<p>
	First, you just have to click on this <a href="natas3.natas.labs.overthewire.org">link</a> and connect using natas3:pw.
Google uses web-crawlers / web-spiders robots to run around every website and read its content.
To display hidden folders that can't be accessed by web crawlers, check the robots.txt file in the server.
The robots text file shows that there is a directory called "S3cr3t" in the server, that has the file users.txt with the pw for the next level.
<!--One tool to catch the files and directories using the website url,  through brute force : dirbuster.-->
</p>

<h3>Natas:level 4</h3>
<p>
	First, you just have to click on this <a href="natas4.natas.labs.overthewire.org">link</a> and connect using natas4:pw.
	you can see a message saying: "Access disallowed. You are visiting from "" while authorized users should come only from "http://natas5.natas.labs.overthewire.org/"", to get access you have to change the referrer to natas5 url, to do so you can add a line in burp's proxy request:
	Referer: http://natas5.natas.labs.overthewire.org/, you then get redirected to a page with a password for the next level

</p>

<h3>Natas:level 5</h3>
<p>
	First, you just have to click on this <a href="natas5.natas.labs.overthewire.org">link</a> and connect using natas5:pw.
	You can see a message saying :"Access disallowed. You are not logged in", after just logging in, but if you search in cookies, you'll find the value of loggedin set to 0. After setting it to 1 and reloading the page we get the password for the next level.

</p>

<h3>Natas:level 6</h3>
<p>
	First, you just have to click on this <a href="natas6.natas.labs.overthewire.org">link</a> and connect using natas6:pw.
	We can see that there is a textbox where you appareently have to paste in the secret code to get the pw for the next level, and a link to the source code of that page. We need the source code beecause we can't see php code from console because it's only stored on the server unlike the html and css code that you can freely navigate. 
In this source code written in php, we see an a file included : "includes/secret.inc" so now we just have to copy paste in with the rest of the url and you'll have to secret code.

</p>
