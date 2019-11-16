# Dev server Soup to Nuts

Use SpringFin projects as my touchstone, though the blog posts themselves should include sample projects so that I don't give up SF IP.

## Pieces I can think of:

	- Git server - include Web (the python one, say - can this be deployed by docker? Nginx can be)
	- Nuget Server - looks like this could be tricky, though there are beginnings of attempts to have this deployed by docker container
	- Git hook to build Nuget for packages (should set up publish branch that it operates on)
	- For test dev of dependency packages, need to figure how to build nuget locally and hot swap for the private one
		- https://www.google.com/search?q=switch+from+nuget+package+to+code+to+make+changes+in+dependent+project&rlz=1C1CHFX_enUS517US517&oq=switch+from+nuget+package+to+code+to+make+changes+in+dependent+project&aqs=chrome..69i57.34959j1j7&sourceid=chrome&ie=UTF-8
	- .NET build stuff should be deployed via docker
	- Private Docker registry for our images (including the Nuget image, etc)
	- SQL deployed in docker
	- Configuration files (with connectionstrings, etc) should be checked in for dev and test. Their values will be unchanged per dev, because they will refer to docker containers that are also defined in source control.