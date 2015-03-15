# Introduction #
Quick Start Guide (Java)


# Details #

The JAR file contains everything you need to get rolling. Here is an example use of the API. be sure to read the doc's for all the options.

```
// create a ZipMyURL instance.
ZipMyURL zmu = new ZipMyURL();
	
// add as many URL's as you like
zmu.addURL("http://www.forbes.com/home/2008/06/15/cellphone-addict-iphone-tech-wireless08-cx_wt0616addict.html");
zmu.addURL("http://www.forbes.com/technology/2008/06/16/solar-intel-ibm-tech-cx_bc_0616techsolar.html?feed=rss_technology");
	
// add keywords/tags (optional) [keywords will be added to del.icio.us posting if you have an account]
zmu.addKeyword("cellphone");
zmu.addKeyword("wireless");
zmu.addKeyword("forbes");
zmu.addKeyword("solar");
	
// If you have an account and you want to automatically post your zipped URL's to twitter and del.icio.us, then add your creds!. 
// If you do enter your account details, the API will automatically connect over SSL to keep your details secure.

zmu.setUserName("my@username.com");
zmu.setUserPassword("mypassword");
	
// zip			
if(zmu.zip()) {
		
	System.out.println("zipped URL: " + zmu.getZippedURL());
	System.out.println("Original Size: " + zmu.getZippedURLOriginalSize());
	System.out.println("Zipped Size: " + zmu.getZippedURLCompressedSize());
	
} else {
	// error!			
	System.out.println("error: " + zmu.getError());
	
}
```

And that's all there is to it!
- Dave <dave@quobix.com>