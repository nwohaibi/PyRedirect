PyRedirect
==========

Get All HTTP Redirection Path. 
When sending HTTP(Ss) you get redirected thru the Location header. This simple Python module returnes all the URLs it passes thru to the final URL. It will try the request thru an HTTP HEAD and if it faild, thru an HTTP GET. HTTP and HTTPS supported.  
This library was made for filtering certain content in private networks.  
Examples:
---
<pre>

http://www.facebook.com/editaccount.php?ref=321
All passed-thru URLs(Full-Path): 
          \__http://www.facebook.com/editaccount.php?ref=321
           \__http://www.facebook.com/settings?ref=321
            \__http://www.facebook.com/login.php
            
http://m.vuclip.com/w?cid=321
All passed-thru URLs(Full-Path): 
          \__http://cutt.us/321
           \__http://soo.gd/32146
            \__http://m.vuclip.com/w?cid=32146
</pre>