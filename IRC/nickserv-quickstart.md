# NickServ quickstart #

The first (and possibly only) things you're going to do with NickServ are:

* register your nick
* verify your nick
* "log in to" your nick

## Registering your nick ##

Log in to the network you want to register a nick on

Register your nick:

    /msg nickserv register $PASSWORD $EMAIL
    
You'll now receive an email with instructions to verify your nick.

Hide your email from other users:

    /msg nickserv set hidemail on

See the info `NickServ` has on you:

    /msg nickserv info
