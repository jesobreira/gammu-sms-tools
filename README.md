# Gammu SMS Tools
**gammu-long-sms**: Send long text SMS (more than 170 characters) using only gammu, without gammu-smsd.

**gammu-flash-sms**: Send flash SMS (class 0, message that shows as popup and does not get saved on the inbox) using gammu

Based on [Gammu's long SMS example](https://github.com/gammu/gammu/blob/master/docs/examples/long-sms.c).

## Downloads

* [\*nix binary](https://github.com/jesobreira/gammu-long-sms/releases)
* (no Windows binaries yet, sorry)

## Compiling

You must have installed gammu and libgammu-dev

```
sudo apt-get install gammu
sudo apt-get install libgammu-dev
```

Finally, compile the needed files:

```
gcc gammu-long-sms.c -o gammu-long-sms `pkg-config --cflags --libs gammu`
gcc gammu-flash-sms.c -o gammu-flash-sms `pkg-config --cflags --libs gammu`
```

## Installing

The binary can be used standalone. If you want to make it accessible from any folder without touching your PATH variable, just move it to /usr/bin:

```
sudo mv gammu-long-sms /usr/bin
sudo mv gammu-flash-sms /usr/bin
```

## Usage

```
gammu-long-sms <number> <message>
gammu-flash-sms <number> <message>
```

Example:

```
gammu-long-sms 011987654321 "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In efficitur gravida diam et tempor. Suspendisse porta molestie ligula, non rhoncus nulla tincidunt et."
gammu-flash-sms 011987654321 "Lorem ipsum dolor sit amet, consectetur adipiscing elit"
```

## Notes

Although this lib allows sending flash SMS with more than 170 characters, it's not recommended to overpass this limit since we can't grant that all devices are able to show long flash messages.

Flash SMS shall only be used for emergency situations such as natural disasters announcements, and never as promotional or advertising messaging.

I'm not and Gammu developers aren't responsible for the misuse of any of these tools or any consequence that the usage of these tools may carry. You may be blocked by your provider if they find out you're misusing your SMS service.
