https://www.scara.com/~schirmer/o/mplex13818/
Copyright (C) GPL 2004..2008, Oskar Schirmer

# mplex13818
# iso 13818 stream multiplexer
 
This multiplexer is designed to run uninterruptedly on a streaming server, 
that propagates a number of iso 13818 broadcast streams, reorganizing the streams in realtime. 
I wrote it in 2001 for convergence gmbh, and they kindly released it finally as open source, 
under the general public license (gpl) in 2003.

# Features:

Output is either a transport stream or a program stream
input streams may be program streams, paketized elementary streams (PES) and transport stream, in any combination
streams are kept in sync during multiplex, where possible.
Normal real time operation obeys stream timing, but untimed operation is available for discfile conversion
program information and stream compilation may be changed on the fly during operation
program map table manipulation, descriptor filter/injection.
Now includes an additional tool for EN 300468 SI table composition

# What this multiplexer does not:

It does neither check, unpack nor recode elementary streams, 
it does not even care for what data it shovels: just bytes
it does not check system performance capacities, so when the cpu cannot do the work, 
timing faults in the resulting stream may occur, even when running it in untimed mode.

# Installation: 

Unpacking archive and "make install" will place it in the /usr/local sub hierarchy. 

No readme file available, but man pages: iso13818ts(1), iso13818ps(1), repeatts(1), en300468ts(1)

There are additional diagnostic tools included: 
showts, ts2pes, pes2es. these are provided by third party, 
so i cannot explain details about them. 
The latter two are said to produce a nice stream dump when given the option -v. 
You are invited to write a man page or similar for these. 
Otherwise check the sources for explanations.
