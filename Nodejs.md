# Node.js

Special thanks to http://joshondesign.com/2013/10/23/noderpi

## Step 1. Download and unzip Node.js for Linux ARM Pi

```bash
# Download v0.10.28 for Linux ARM Pi
wget http://nodejs.org/dist/v0.10.28/node-v0.10.28-linux-arm-pi.tar.gz
# Unzip
tar -xvzf node-v0.10.28-linux-arm-pi.tar.gz
```

You can see all downloads at http://nodejs.org/dist/

## Step 2. Install Node.js `bin`

Set the `NODE_JS_HOME` variable to the directory where you un-tarred Node.
Next, add the `bin` directory to your `PATH` environment variable.

```bash
NODE_JS_HOME=/home/pi/node-v0.10.28-linux-arm-pi
PATH=$PATH:$NODE_JS_HOME/bin
```

The above could go in your `~/.bash_profile`.

## Step 3. Test

You should now be able to run both `node` and `npm`.

```bash
node --version
npm -version
```
