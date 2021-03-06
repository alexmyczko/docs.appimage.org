# Testing your AppImage

Testing your AppImage  is a very important step inproducing an AppImage.
Since AppImage  files are supposed to run on a variety of Linux distributions, it is important to test your AppImage 
on a wide variety of distributions.

__Test your AppImage__ on all base operating systems you are targeting. 
This is an important step which you should not skip. Subtle differences in distributions make this a must. 
While it is possible in most cases to create AppImages that run on various distributions, this does not come automatically, 
but requires careful hand-tuning.

To ensure that the AppImage runs on the intended base systems, it should be thoroughly tested on each of them. 
The following testing procedure is both efficient and effective: 
Get the previous version of Ubuntu, Fedora, and openSUSE Live CDs and test your AppImage there. 
Using the three largest distributions increases the chances that your AppImage will run on other distributions as well. 
Using the previous (current minus one) version ensures that your end users who might not have upgraded to the latest version
yet can still run your AppImage. 

Using Live CDs has the advantage that unlike installed systems, 
you always have a system that is in a factory-fresh condition that can be easily reproduced. 
Most developers just test their software on their main working systems, 
which tend to be heavily customized through the installation of additional packages. 
By testing on Live CDs, you can be sure that end users will get the best experience possible.

## Using testappimage

You can use ISOs of Live CDs, loop-mount them, chroot into them, and run the AppImage there. 
This way, you need approximately 700 MB per supported base system (distribution) and can easily upgrade to newer 
versions by just exchanging one ISO file. 
The following script automates this for Ubuntu-like (Casper-based) and Fedora-like (Dract-based) Live ISOs:

```
sudo ./testappimage /path/to/elementary-0.2-20110926.iso ./AppImageAssistant.AppImage
```
