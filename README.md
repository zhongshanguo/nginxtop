# Nginxtop

UNIX top-like app for nginx (or Apache, if you wish) access logs.

Every so often, a poorly behaved spammer or web crawler will hit one of the websites 
I manage, and proceed to load the same pages over and over, causing a resource issue 
and possibly even a Denial of Service.  I got tired of this, so I built my own tool to determine 
in real time who the culrprits were.


## Installation

### Via npm (recommended)

    npm install -g nginxtop
    
This will install nginxtop into /usr/local/bin/ or somewhere else likely to be in your path.


### From source

    git@github.com:dmuth/nginxtop.git
    cd nginxtop

This will check out a copy of the nginxtop app to your current directory.


## Usage

    tail -f /var/log/nginx/access.log | nginxtop [ -n num_hosts_to_print] [-i report_interval_in_seconds]

    
## Testing

There is a file called `test.log` in this directory.  It contains sample log entries.  To test nginxtop using it:

    tail -fn100 test.log | nginxtop -n 5

You'll start to see output like this once every second:

                 Nginxtop Top Hosts
    ===========================================
                        127.0.0.10:     14 hits
                         127.0.0.1:      7 hits
                         127.0.0.2:      6 hits
                         127.0.0.3:      6 hits
                         127.0.0.4:      5 hits


## Where to find this

- [https://bitbucket.org/dmuth/nginxtop](https://bitbucket.org/dmuth/nginxtop)
- [https://github.com/dmuth/nginxtop](https://github.com/dmuth/nginxtop)


### Feedback

Have feedback?  Want to report bugs?

Hit me up via email (doug.muth@gmail.com) or via many other methods listed at:
[http://www.dmuth.org/contact](http://www.dmuth.org/contact)

Enjoy!



