# Control Raspberry Pi GPIO via http web server

This repository contains python code for demostrating on how to control Raspberry Pi GPIO via a simple http server implemented using python standard library http.server. The http.server library allows user to create its own http request handler class to handle the GET and POST requests.

In the `simple_webserver.py` example provided. the `do_GET()` method creates an html template which read some data from the Raspberry Pi and provide an html interface for user to interact with the server. The `do_POST()` method parse the post request sent by the browser and use its value to control the Raspberry Pi GPIO.

In the `simple_webserver2.py` example, it deomonstrates how to handle multiple GET requests based on various URL endpoints.

For more details about the codes, refer to my blog post [How to control Raspberry Pi via http web server](https://www.e-tinkers.com/2018/04/how-to-control-raspberry-pi-gpio-via-http-web-server/).

[YouTube demostration](https://youtu.be/SRf6HW_b3EE)

### Alternative - Using Node-RED
[Update - Feb, 2019] When I wrote this python code and the article almost a year ago, I never expect the article became one of the most popular posts on my blog. The reasons that I wrote this code were 1) to demonstrate that you probably don't need to install a web framework and a full feature web server, especially if you are new into programming, using web framework and setup web server could be overwhelming; 2) to demonstrate how socket and http communication works.

However, the approach that I took of using socket to implement http is likely not scalable for complex GPIO project, for that, you probably need a proper web framework, or alternatively, for those came from hardware background or new to programming, you should take a look at the "[examples on using node-RED](https://github.com/e-tinkers/simple_httpserver/tree/master/examples%20using%20node-RED)" directory which achieves the same result with almost no programming required.
