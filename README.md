# Redirect HTTP
This is a simple script to read in a parameter from the URL and then redirect based on a lookup in a CSV file. <br>
I guess you could call this a manual version of ow.ly or bit.ly.<br>
  
If scripting is disabled, the site redirects to the default URL (line #6).<br>
  
The script reads the source URL and looks for the value of Prod (line #18).<br>
For example:  http://site.com/page.html?Prod=12345<br>
  
Some simple tests are done to ensure this is a valid product number:
 - contains 5 characters
 - numbers only
  
This value is then searched for in a CSV file (specified in line #14 _lookupfile_ <br>
The resulting value is first confirmed to be a valid URL, and then the page is redirected to that URL. <br>
If there are any errors found, the code redirects to the default URL. <br>
  
Customising for your own use:
 - Line #4 - update canonical name of file
 - Line #6 - update default location for noscript
 - Line #14 - location of CSV file - _lookupFile_
 - Line #16 - default URL to redirect to - _destinationURL_
 - Line #18 - query string to search for in the URL - _prodCode_
