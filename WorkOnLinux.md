## Working with "propeller" on Linux


Using the Spin2 extension for VS Code.

![alt text](image.png)

Then using openspin to compile and proploader to load to RAM or EEPROM.


### Compiling with openspin

``` bash
openspin -o busfinder.eeprom -e -v JTAGulator.spin

```

### Write to RAM with proploader

``` bash
sudo proploader -p /dev/ttyACM0 -v busfinder.eeprom 
```

### Write to EEPROM with proploader
``` bash
sudo proploader -p /dev/ttyACM0 -e -v busfinder.eeprom 
```

## Installing the tools:

### Installing openspin

``` bash
wget -U 'Mozilla/5.0 (X11; Linux x86_64; rv:148.0) Gecko/20100101 Firefox/148.0' https://www.maccasoft.com/wp-content/downloads/openspin_1_00_81-linux-x86_64.tar.gz
tar -xzvf openspin_1_00_81-linux-x86_64.tar.gz
chmod 755 openspin
sudo mv openspin /usr/bin/
```

### Installing proploader
wget https://github.com/parallaxinc/PropLoader/releases/download/v1.0-37/proploader-linux.zip
unzip proploader-linux.zip 
chmod 755 proploader
sudo mv proploader /usr/bin/


