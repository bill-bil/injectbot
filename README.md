![Scan SQL Injection](https://www.tariqhawis.com/img/injectbot/injectbot-flag.png)

# InjectBot&trade;

A web-based, easy-to-use, SQL injection scanner and exploiter tool. 

# Why InjectBot?

Unlike other SQLi tools out there, InjectBot is so simple to use, yet very fast compared to other SQL tools. (*like 1 to 10 faster!!*)

* InjectBot is as simple as Google with web search; A input box to provide the target, and a list of scan/attack options, and finally a terminal-like screen to show the results of the scanning.

* In case the provided target is vulnerable to SQLi, InjectBot will save the target's state with a small rectangle indicating the saved target, and any next scan/attack actions performed will be saved for you to speed up the scan and cut any repeatable steps during the scan on the target. Then whenever you finish with the target, just click on the `x` mark (See the demo down below..).


**Current Features:**

* Scan the target only to see if whether it's vulnerable.

* Get target's database and server information.

* Get tables information from the current database.

* Fetch data rows of selected table (select from the table list saved previously).

* Switch between classic and blind SQLi in options above.


# DEMO

A complete scan to a web app showing all the above features in only 23 seconds.

![InjectBot SQLi scanning Demo](https://www.tariqhawis.com/img/injectbot/injectbot.gif)


# Who should use InjectBot?

Whether you are a web developer or pen tester, red or blue teamer, this tools would be perfect to be in your tools arsenal to test web applications against SQL Injection vulnerabilities.


# Requirements

* Option #1: Use Docker engine to pull and run injectbot image as described under installation section below, for more details about how to use docker, refer to [Docker Docs](https://docs.docker.com/get-docker/)

* Option #2: A need your own web server up and running and have PHP 7.4 plus php-curl library.


# Installation

The easiest way is to use the docker image which already has injectbot installed & updated at docker hub, just run this below command:

```bash
docker run --name injectbot -d -p 8080:80 tariqhawis/injectbot:latest
```

If you have not received any error message, go to the URL: `http://localhost:8080/`
Now Injectbot is up and running.

Second option is to clone this repository and point your web server to cloned path.

If you have any issue with installation, contact me at [github issues](https://github.com/tariqhawis/injectbot/issues), and I will be glad to help:)


# Version History/Changelog

InjectBot v1.0 - rebuild and published release from the old private 0.5 Injectbot 2009.

* [+] Complete transition from procedural to object-oriented structure.
	* [-] Troubleshooting has become much easier with modularity.
	* [-] Scalability is now possible, adding features such as new SQLi techniques is much easier.
	* [-] The code structure is understandable, any developer who wants to jump in can understand the idea of each step, also comments added for that purpose.

* [+] Increase the speed of HTTP response by 20 times
	* [-] Use Multi cURL functions instead of file_get_contents for faster response.
	* [-] Ability to send multi requests in parallel.
	* [-] Send header requests for blind SQLi.
	* [-] Use content-length from the header instead of str_len for the whole page!

* [+] Remove iterations by saving scanning state.
	* [-] Use sessions to save the state of the target while the scanning progress.

* [+] Add blind SQLi scanning mode for fetching table schema and data records

* [+] Bugfixes
	* [-] Fixed content-length with returned -1.
	* [-] Fixed exploitable number inside html tags for some webpages.

* [+] New front-end design based on Bootstrap 4.


# Have an idea for InjectBot?

There are plenty of improvements this script could use, If you want to add something and have any cool idea related to this tool, please contact me using [github issues](https://github.com/tariqhawis/injectbot/issues) and I will update the master version.

If you are a PHP developer yourself, feel free to PR this tool, and I will merge the good ideas.


# Looking for a useful SQL Injection Course?

Contact me if you are looking for a course on web penetration testing, web application security, or a course explosively on SQL Injection, I am preparing for attackers and defenders (100% technical).


# Advisory

This tool should be used for authorized penetration testing and/or educational purposes only. 
Any misuse of this software will not be the responsibility of the author or of any other collaborator. 
Use it at your own networks and/or with the network owner's permission.


GPL-3.0 License 2020 InjectBot&trade; - By Tariq Hawis
