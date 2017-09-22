# gammu-long-sms
Send long text SMS (more than 170 characters) using only gammu, without gammu-smsd.

Based on [Gammu's long SMS example](https://github.com/gammu/gammu/blob/master/docs/examples/long-sms.c).

## Downloads

* [\*nix binary](https://github.com/jesobreira/gammu-long-sms/releases)
* (no Windows binaries yet, sorry)

## Compiling

You must have installed gammu and libgammu-dev

```
sudo apt-get install gammu
sudo apt-get install libgammu-dev`
```

Finally, compile it:

```
gcc gammu-long-sms.c -o gammu-long-sms `pkg-config --cflags --libs gammu`
```

## Installing

The binary can be used standalone. If you want to make it accessible from any folder without touching your PATH variable, just move it to /usr/bin:

```
sudo mv gammu-long-sms /usr/bin
```

## Usage

```
gammu-long-sms <number> <message>
```

Example:

```
gammu-long-sms 011987654321 "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In efficitur gravida diam et tempor. Suspendisse porta molestie ligula, non rhoncus nulla tincidunt et. Donec dapibus lobortis neque, eu bibendum ex. Nullam non venenatis augue. Vestibulum sodales, lectus vel faucibus lacinia, eros justo bibendum leo, ut sodales lectus orci sit amet dui. Maecenas nec sem lorem. Donec tempor mi ultrices, elementum sapien id, porttitor magna. Fusce sagittis facilisis mollis. Nulla id ante at urna massa nunc."
```
