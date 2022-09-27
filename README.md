# Practice Awk

Practice `awk` (Program File).

```bash
# MacOS BSD Awk
$ awk --version
awk version 20200816
# GNU Awk
$ gawk --version
GNU Awk 5.1.1, API: 3.1 (GNU MPFR 4.1.0, GNU MP 6.2.1)

# Awk File
$ cat ./example.awk
#!/usr/bin/awk -f
{ printf "%-20s %s\n", $1, $2 }

# `-f` : BSD And GNU Awk
$ cat << EOL | awk -f ./example.awk
hoge-server RUNNING
fugafuga-server STOPPED
foo-server RUNNING
something-server RUNNING
EOL
hoge-server          RUNNING
fugafuga-server      STOPPED
foo-server           RUNNING
something-server     RUNNING

# `--file` : GNU Sed Only
$ cat << EOL | gawk --file ./example.awk
hoge-server RUNNING
fugafuga-server STOPPED
foo-server RUNNING
something-server RUNNING
EOL
$ cat << EOL | gawk --file='./example.awk'
hoge-server RUNNING
fugafuga-server STOPPED
foo-server RUNNING
something-server RUNNING
EOL
```


## Links

- [Neo's World](https://neos21.net/)
