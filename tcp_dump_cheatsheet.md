## TCPDUMP

cpdump is a commandline tool that is used to dump traffic on a network. This tool comes in hand when you want to analyse network captures within the command line. Basically it can do most of the wireshark job.


NOTE This guide might not be complete it just serve as a reference to me.
<hr>

## Additional Note & Reference

To be fair: This gist is itself a fork I created some time ago, but the original gist or author seems to not exist anymore, and it looks like that I'm now in the lead ;-) Please see the revision history for details.

Furthermore some more and basic advanced examples may be of interest (thanks to twitter://@howtouselinux1):

[Tcpdump Cheat Sheet (Basic Advanced Examples)]:(https://howtouselinux.com/post/tcpdump-cheat-sheet)/"Tcpdump Cheat Sheet (Basic Advanced Examples)"


## Options

The following are some of options that I prefer when using tcpdump for my daily use.

tcpdump [OPTIONS]

-i any : Listen to all the interfaces

-i virbr0: Listen to a specific interface virbr0

-D: Show the list of available interface

-n: Don't resolve the hostnames

-nn: Don't resolve hostnames or port names.

-q: quite output

-t: Don't print a timestamp on each dump line.

-tttt: Give maximally human-readbale timestamp output

-X: Show the packet's contents in both HEX ad ASCII

-XX: Same as -X but shows the ethernet header.

-v, -vv, -vvv: Being more verbose(increase number of packet information)

-c: Only capture number of packets and stop

-s: Define the snaplength(size) of the capture in bytes. Use -s0 to get
everything.

-S: Print absolute sequence numbers.

-e: Get the ethernet header as well

-E: Decrypt IPSEC traffic by providing an encryption key.

## Expressions

tcpdump allow us to use expression so we can narrow down our solution to get exactly what we're looking for.

There are 3 types of expression: type, dir and proto

-Type options are: host,net, and port

-Direction are: src and dst

-Protocol : tcp,udp,icmp,ah etc

https://gist.github.com/jforge/27962c52223ea9b8003b22b8189d93fb#expressions

THM : Room : Layer2

