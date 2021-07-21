# Vulnado - Intentionally Vulnerable Java Application

[![HIPAA](https://app.soluble.cloud/api/v1/public/badges/585d9e75-80d5-44d6-8703-40c5310ef775.svg)](https://app.soluble.cloud/repos/details/github.com/lingom-ksr/vulnado)  [![IaC](https://app.soluble.cloud/api/v1/public/badges/709eb46c-0720-4f26-bf17-d3f1ffafc80d.svg)](https://app.soluble.cloud/repos/details/github.com/lingom-ksr/vulnado)  [![CIS](https://app.soluble.cloud/api/v1/public/badges/9b24c35e-aaee-451f-a90e-45382b320024.svg)](https://app.soluble.cloud/repos/details/github.com/lingom-ksr/vulnado)  

This application and exercises will take you through some of the OWASP top 10 Vulnerabilities and how to prevent them.

## Up and running

1. Install Docker for [MacOS](https://hub.docker.com/editions/community/docker-ce-desktop-mac) or [Windows](https://hub.docker.com/editions/community/docker-ce-desktop-windows). You'll need to create a Docker account if you don't already have one.
2. `git clone git://github.com/ScaleSec/vulnado`
3. `cd vulnado`
4. `docker-compose up`
5. Open a browser and navigate to the client to make sure it's working: [http://localhost:1337](http://localhost:1337)
6. Then back in your terminal verify you have connection to your API server: `nc -vz localhost 8080`

## Architecture

The docker network created by `docker-compose` maps pretty well to a multi-tier architecture where a web server is publicly available and there are other network resources like a database and internal site that are not publicly available.

![](exercises/assets/arch.png)

## Exercises

* [SQL Injection](exercises/01-sql-injection.md)
* [XSS - Cross Site Scripting](exercises/02-xss.md)
* [SSRF - Server Side Request Forgery](exercises/03-ssrf.md)
* [RCE - Remote Code Execution & Reverse Shell](exercises/04-rce-reverse-shell.md)
