# SharpRoast-Parser
Bash one-liner that will parse harmj0y's SharpRoast into hashcat crack-able format.

**cat kerberoast.txt | grep Hash -A 29 | sed 's/\<Hash\>//g' | sed s/://g | sed s/--//g | sed -r 's/\s+//g' | tr '\n' ' ' | sed 's/\s//g' | sed 's/$k\{1,\}/\'$'\n&/g' > kerb_hashes_hashcat.txt**

https://grumpy-sec.blogspot.com/2018/08/kerberoasting-and-sharproast-output.html




cat kerberoast.txt | grep Hash -A 42 | sed 's/\[\*\]\ Hash//g' | sed s/://g | sed s/--//n&/g'ed -r 's/\s+//g' | tr '\n' ' ' | sed 's/\s//g' | sed 's/$k\{1,\}/\'$'\n
