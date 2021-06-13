# Salesforce Commerce Cloud - Local Code setup #

1. Clone project repository url(bitbucket) and integrate using eclipse.

```
	* Login to bitbucket 
	* Choose project repository('respective repository' > 'clone button' > copy 'clone Url')
```	
	Open Eclipse:
```	
	* Windows > Perspective > Open Perspective > other
	* From Popup window select 'Git' > Open
	* click on "Clone Git Repository" ('popup window')
	* paste clone url from bitucket in "URI" field
	* Add user/password of bitbucket.
	* Click 'Next' > select 'development branch' > select 'All catridge' > Ok.
	
	  - Now selected cartridge will be available in local workspace
```
	Import the cartridge to eclipse:
```	
	* how to open 'Digital Development' Perspective
		 Windows > Perspective > Open Perspective > other
		 From Popup window select 'Digital development' > Open
		 
	* Right Click on 'Navigator' window (Import > Existing Project into window > Next > Browse your wrorkspace > Select the cartridge> Next
```	

2. Install UX Studio:

```
	* UX Studio is a plug-in for Eclipse IDE for Java EE Developers.
	* The UX Studio plug-in requires JDK 8 and supports the following Eclipse versions.
		- Mars - Eclipse 4.5
		- Neon - Eclipse 4.6
	* In Eclipse, Go to "Help" > Install New Software > Add
	* Enter "UX Studio" as the name.
	* Enter a location according to your Eclipse version and instance type. To access different instance types, install different Eclipse instances with different Studio versions.

		If use Mars, then
		https://developer.salesforce.com/media/commercecloud/uxstudio/4.5

		If Neon, then
		https://developer.salesforce.com/media/commercecloud/uxstudio/4.6

	* Select Salesforce B2C Commerce, and click Next.
	* Eclipse verifies compatibility and Click Next.
	* Select the license agreements, and click Finish.
	* When the installation completes, click Yes to restart Eclipse.

	Note : If you experience problems, make sure that JDK 8 is installed.
```

3. Create a code-version in local sandbox:

```
	Business Manager:
	* Administration -> Site Development -> Code deployment
	* Click Add
	* Enter Code version 
		eg: SFRA_Spain (It can can any combination of letters)
	* Click Apply
	* Click on Activate link for this newley code version
```

4. Create a new Digital Server connection

```
	* In Eclipse, File -> New -> Digital Server connection
	* Enter hostname eg: dev04-apacestore-pandora.demandware.net
	* Enter Username and password (Use same username and password using to open local sandbox 
		i.e, Business manager password))
	* Click Next
	* In Target version select the code version that created in above step(#3)
	* Click Finish.
```	

5. Your project is now connected to your sandbox. It will be used to upload any cartridge projects to that sandbox.


6. How to do npm Installation:

```
	* Open command prompt in the location where your package.json file residence from your local workspace
		Use below npm command one by one
			1. npm install
			2. npm run build-dev 

	* Once npm command ran successfully , refresh the eclipse to upload the changes into sandbox
```
	
