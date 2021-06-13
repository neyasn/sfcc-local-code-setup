# sfcc-local-code-setup

1. How to clone project repository(bitbucket) using eclipse.

	* Login to bitbucket 
	* Choose project repository('respective repository' > 'clone button' > copy 'clone Url')

2. Open eclipse
	* Windows > Perspective > Open Perspective > other
	* From Popup window select 'Git' > Open
	* click on "Clone Git Repository" ('popup window')
	* paste clone url from bitucket in "URI" field
	* Add user/password of bitbucket.
	* Click 'Next' > select 'development branch' > select 'All catridge' > Ok.
	
Now selected cartridge will be available in local workspace

3. How to import the cartridge to eclipse 
	3.1 Open 'Digital Development' Perspective
	* Windows > Perspective > Open Perspective > other
	* From Popup window select 'Digital development' > Open
	* Right Click on 'Navigator' window (Import > Existing Project into window > Next > Browse your wrorkspace > Select the cartridge> Next
	
4. Install or Update UX Studio
UX Studio is a plug-in for Eclipse IDE for Java EE Developers.

The UX Studio plug-in requires JDK 8 and supports the following Eclipse versions.
	* Mars - Eclipse 4.5
	* Neon - Eclipse 4.6

4.1 How to install UX studio?
	* In eclipse, Go to "Help" >Install New Software
	* Click Add
	* Enter "UX Studio" as the name.
	* Enter a location according to your Eclipse version and instance type. To access different instance types, install different   Eclipse instances with different Studio versions.

If you are using Mars
https://developer.salesforce.com/media/commercecloud/uxstudio/4.5

If you are uisng Neon
https://developer.salesforce.com/media/commercecloud/uxstudio/4.6

	* Select Salesforce B2C Commerce, and click Next.
	* Eclipse verifies compatibility.
	* Click Next.
	* Select I accept the terms of the license agreements, and click Finish.
	* When the installation finishes, click Yes to restart Eclipse

Note : If you experience problems, make sure that JDK 8 is installed.


5. Create a New code version in local sandbox:
	* Administration -> Site Development -> Code deployment
	* Click Add 
	* Enter Code version eg: SFRA_Spain (It can can any combination of letters)
	* Apply
	* Click on Activate link for this newley code version


6. Create a new Digital Server connection
	* In Eclipse , File -> New -> Digital Server connection
	* Enter hostname eg: dev04-apacestore-pandora.demandware.net
	* Enter Username and password (Use same username and password using to open local sandbox i.e, Business manager password))
	* Click Next
	* In Target version select the code version that created in above step
	* Click Finish

Your project is now connected to your sandbox. It will be used to upload any cartridge projects to that sandbox.

7. How to do npm Installation

Open command prompt in the location where your package.json file residence from your local workspace
Use below npm command one by one
	1. npm install
	2. npm run build-dev 

Once npm command ran sucesfully , refresh the eclipse to upload the changes into sandbox
