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

* chute/index.html: is a default HTML page.  It will display the
results from results.txt.  Feel free to modify the HTML as you
see fit.  It will be installed to /usr/share/nginx/html/index.html
inside the chute.

* chute/results.txt: is an empty text file where you can write test
results for displaying.  It will be installed to
/usr/share/nginx/html/results.txt inside the chute.

## Getting Started

1. Fork this project to your own github account.
2. Add your code for testing network performance.  Some helpful commands are [ping](http://manpages.ubuntu.com/manpages/trusty/man8/ping.8.html) and [iperf](http://manpages.ubuntu.com/manpages/trusty/man1/iperf.1.html).  The university maintains an iperf server (iperf.wiscnet.net), which you can use.  See [here](https://kb.wisc.edu/wiscnet/page.php?id=9009) for more information.
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
