# keys, password manager 

![keys.png]()

## example usage

create a database:

```
how strong do you want your scrypt KDF settings? ([a]/b/c/d/e/f/0)
a) weak ~1 seconds / 0.5GB RAM (19/8/1)
b) medium ~2 seconds / 1GB RAM (20/8/1)
c) hard ~4 seconds / 2GB RAM (21/8/1)
d) pro ~8 seconds / 4GB RAM (22/8/1)
e) max ~16 seconds / 8GB RAM (23/8/1)
f) extreme ~32 seconds / 16GB RAM (24/8/1)
0) experimental (unsafe) 100 ms / 65MB RAM (16/8/1)
d⏎
enter new master key:⏎
repeat it:⏎
created at /home/test/.key_database/key_database

```

add a new entry:

```
$ keys add
type the new title: gmail⏎
type the new username [press enter for random]: john@gmail.com⏎
type the new password [press for random]:⏎
type the new TOTP key:⏎
type a note:⏎
doing changes to the database... important: do not delete or change any temporary files now
```

get a list of all your entries:

```
$ keys list -l
1. gmail/john@gmail.com
2. github/john@gmail.com
```

copy to clipboard an entry including the word "gmail":

```
$ keys copy gmail
gmail/john@gmail.com copied, clearing clipboard in 20
```

## tips and tricks

display all your entries in a fancy way:

```
keys list -ln | sed 's./.\t.g' | column -t -s "$(printf '\t')"
```

find an entry by the contents of its password:

```
$ keys get cows
gmail/palse68
tall cows layout karen battle field
```
