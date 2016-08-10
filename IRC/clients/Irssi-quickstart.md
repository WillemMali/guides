# Irssi quickstart #

Open irssi:

    irssi

Add a network:

    /network add -nick $YOURNICK -user $YOURUSER

For instance:

    /network add -nick WillemMali -user WillemMali

Add a server for the network you just added (you can have multiple alternative servers for each network):

    /server add -noauto -network freenode irc.freenode.net

Connect to the network:

    /connect freenode

And you're in! Now go [register your nick with NickServ](../NickServ-quickstart.md).
