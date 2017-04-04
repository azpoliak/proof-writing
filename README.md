This repo contains the 3 scripts described in 
http://matt.might.net/articles/shell-scripts-for-passive-voice-weasel-words-duplicates/
to point out: "weasel" words, passive voice, and duplicate words in a paper.

Look for through the short blog post for more details. 

Instructions:
----
1. Add the subdirectory bin/ in the directory with your source .tex files.
1. Add the following to your Makefile:
```
# Check style:
proof:
        echo "weasel words: "
        sh bin/weasel *.tex
        echo
        echo "passive voice: "
        sh bin/passive *.tex
        echo
        echo "duplicates: "
        perl bin/dups *.tex
```

Example:
----
To test out the functionality of the scripts, clone the repo and run the following
command: ```make proof```.
