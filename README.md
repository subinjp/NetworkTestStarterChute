# Network Test Starter Chute

This Paradrop chute runs periodic network tests and displays the results
through a web server.

## Files

* Dockerfile: specifies the packages and files to install in the chute.
Modify this file if you add new files or need to install other
dependencies.

* chute/run.sh: is the default entry point when the chute runs.  You
should add code here to run latency and bandwidth tests and save the
results.

* chute/index.html: is a default HTML page.  You should add logic to
display the test results.

## Getting Started

1. Fork this project to your own github account.
2. Add new functionality.
3. Launch it on your Paradrop router through paradrop.org.

When creating a version of this chute, you should configure it as shown
in the image.  This chute does not require an additional WiFi AP, but
you should enable port binding as shown.

![Create version options](/images/create_version.png)

After installing the chute on your router, if everything is configured
correctly, you should be able to connect a device to the router's WiFi AP
and access your web server at http://192.168.1.1:8000.  192.168.1.1 is
the local IP address of the Paradrop router, and port 8000 is what we
configured as the external port above.
