# FFmpegBuilder
Script to compile and build ffmpeg on debian based systems (Ubuntu, Mint ..etc)

fmpeg_build - a script to perform all the actions described at:
https://trac.ffmpeg.org/wiki/CompilationGuide/Ubuntu Compile FFmpeg for Ubuntu, Debian, or Mint

The script follows this wiki entry step by step. 
It is intereactive and will ask you simple questions to do its job. 
It is well commented and includes some the associated wiki texts.
I hope the folks at ffmpeg dont mind :) 
I've also included comments about any gotchas I encountered and how I overcame them, if I did and appropriate comments to show what I havent overcome yet.

I've targeted this specifically and nvidia gpus for on chip and ultimateley faster encoding and transcoding
This was my sole purpose for building this script BUT you can choose not to do 
the cuda and nvidia stuff and all will still work - maybe - there might be some things in the configuration function to comment out
If there is I can maybe make it optional - down the track - let me know - or even contribute.

You should read the code in one window and have the wiki page open in another if you want to check its accuracy. 
Rest assured tho, you can just create a ~/ffmpeg folder, switch to it and then run the script in that folder it in the folder. 
It will ask you if you want to perform any all or no steps and if you want it to run all without prompting
or run them in sequence giving you the chance to bail out after any step
The script will stop if any compilation step fails

There are so many gotchas whe you try and follow the original docs at :
https://trac.ffmpeg.org/wiki/CompilationGuide/Ubuntu Compile FFmpeg for Ubuntu, Debian, or Mint
I cant really tell you them all - but my code can tell you some of them

Changes:

I've replaced a few wgets with git clones this is faster - especially for repeated runs
locked the ffmpeg version at release 7.0  to get the whole thing a little more reliable build wise
I've stuck a whole heap more dependancies in for apt-get
Added code to pass nvidia gpu gencode flags to the ffmpeg build - And no you dont have to
    look it up on a web site somewhere - the script will use nvidia-smi to extract that info


This script was written with teaching and learning in mind.
I started programmin in the dark ages and have always opted for very clear and easy to read code.
Mostly because I hated commenting....
So, many years after writing (coding) a thing I might revisit it and call myself names, 
saying "what the %%*$ were you thinking?" (to myself)
Now I try to do both, wright self documenting code AND comment it so that this (me) complete eedjit can work out what he did ;)

It aint beautiful code but I reckon most newbies could figure out whats going on.

Hope it works for you ... 
