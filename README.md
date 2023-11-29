# Mathias Sackey Kong-Docker Intern Project
The above project is built for IntegrationWorks to demonstrate Kong API manager working on a Docker container.

## Setting up Kong in Docker
- The project uses docker containers to run Kong. If you are yet to install docker, you may naviagate [here](https://docs.docker.com/get-docker/) to find it. Choose the option most appropriate to your operating system. 
- Clone or Download the repository from GitHub
- Navigate to the location of the yaml file
- Run **docker-compose up** in the command line to build the container with kong running
- Navigate [here](http://localhost:8002)to view the functional Kong Workspace.

## Running KONG MANAGER
### Creating a service
- Once KONG MANAGER is up and running, navigate to the default workspace tab
- From there, click on gateway services and the "+ New Gateway Service" tab
- Enter a name
- Choose protocol, host, port and path under traffic
- Set Host to - "httpbin.org"
- Set Path to "/anything"
- Save your newly created service

### Creating a route
- Navigate to Routes and click on the "+ New Route" tab
- Select the service associated with your route
- Set the http method to "GET"
- Save your newly create route

### Service Verification
- From your web browser, navigate to (http://localhost:8000/anything)
- If your output is similar to below, then your service has been successful. 
{
    "args": {},
    "data": "",
    "files": {},
    "form": {},
    "headers": {
        "Accept": "text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7",
        "Accept-Encoding": "gzip, deflate, br",
        "Accept-Language": "en-US,en;q=0.9",
        "Cache-Control": "max-age=0",
        "Content-Length": "0",
        "Host": "httpbin.org",
        "Sec-Ch-Ua": "\"Microsoft Edge\";v=\"119\", \"Chromium\";v=\"119\", \"Not?A_Brand\";v=\"24\"",
        "Sec-Ch-Ua-Mobile": "?0",
        "Sec-Ch-Ua-Platform": "\"Windows\"",
        "Sec-Fetch-Dest": "document",
        "Sec-Fetch-Mode": "navigate",
        "Sec-Fetch-Site": "cross-site",
        "Sec-Fetch-User": "?1",
        "Upgrade-Insecure-Requests": "1",
        "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/119.0.0.0 Safari/537.36 Edg/119.0.0.0",
        "X-Amzn-Trace-Id": "Root=1-65669806-29f2a29a61ad5f9404a99e8c",
        "X-Forwarded-Host": "localhost",
        "X-Forwarded-Path": "/anything",
        "X-Kong-Request-Id": "b9bcd154d544c26a76bc475ee9367e7f"
    },
    "json": null,
    "method": "GET",
    "origin": "172.18.0.1, 203.86.192.144",
    "url": "http://localhost/anything/anything"
}
