You've heard of terrible, incredibly niche tools, now get ready for to.rc!

Run to.rc from OSS with the command: ENV=to.rc sh


to.rc is a sort of cousin to my tool Orc, but far less useful or interesting.
It's designed for people who may occasionally do Tandem/HP NonStop audits.
You'll still have to do most of the stuff by hand, because I'm lazy, and also
because a lot isn't easily automatable.
However, Torc will help with some basic checks:

- getusers - lists users
- getuserid - get the equivalent of /etc/shadow on NonStops (only as super.super)
- ossinfo - gets some useful info from OSS
- getinfo [file] - gets file info from FUP. Arg is full OSS path, eg /G/system/system/userax
- procinfo [cpu id,pin] - gets user, oss process name or process id from #processinfo builtin.
- getnodes - checks if there are any Tandem machines connected to us via EXPAND.
- netstat - does a verbose netstat
- gettaclconf - checks for nochangeuser remotesuperid. 0 and -1 are the desired output.
- blankpass - checks to see if any users have no password via the #changeuser builtin.
- getroute

TODO:
- enumerate all the $ZTCP files instead of just going for $ZTCP1
- work on translating Guardian permissions into UNIX permissions 
- safeguard ACLs
- check for interesting/useful permission issues - TACLCSTM being writeable etc
- maybe check for $CMON?
