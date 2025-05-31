## knktwce: TOTP SYN port knocking

All credit goes to https://github.com/jvinet/knock and Judd Vinet <jvinet@zeroflux.org>

### ABOUT  

This is just a fork with TOTP support instead of static port knocking code.

This is a port-knocking server/client.  Port-knocking is a method where a
server can sniff one of its interfaces for a special "knock" sequence of
port-hits.  When detected, it will run a specified event bound to that port
knock sequence.  These port-hits need not be on open ports, since we use
libpcap to sniff the raw interface traffic.


### BUILDING

To build knockd, make sure you have libpcap and the autoconf tools
installed. Then run the following:

    $ autoreconf -fi
    $ ./configure --prefix=/usr/local
    $ make
    $ sudo make install

