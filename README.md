# SharpRoast-Parser
Bash one-liner that will parse harmj0y's [SharpRoast](https://github.com/GhostPack/SharpRoast) into hashcat crack-able format.

```bash
cat kerberoast.txt | grep Hash -A 42 | sed 's/\<Hash\>//g' | sed s/://g | sed s/--//g | sed -r 's/\s+//g' | tr '\n' ' ' | sed 's/\s//g' | sed 's/$k\{1,\}/\'$'\n&/g' > kerb_hashes_hashcat.txt
```

https://grumpy-sec.blogspot.com/2018/08/kerberoasting-and-sharproast-output.html



# Rubeus-Parser
Bash one-liner to parse GhostPack's [Rubeus](https://github.com/GhostPack/Rubeus) kerberoast module output into hashcat crack-able format.

```bash
cat kerberoast.txt | grep Hash -A 42 | sed 's/\[\*\]\ Hash//g' | sed s/://g | sed s/--//g | sed -r 's/\s+//g' | tr '\n' ' ' | sed 's/\s//g' | sed 's/$k\{1,\}/\'$'\n&/g'
```

## NOTE:
- View README.md in 'raw' format to copy paste or you will get weird format errors.
- You must adjust the 'grep Hash -A 42' to capture the full hash
