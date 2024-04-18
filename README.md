# examples

## example usage

add a new entry:

```
$ keys add
open database found
type the new title: gmail
type the new username [press enter for random]: john@gmail.com
type the new password [press for random]:
type the new TOTP key:
type a note:
open database found
doing changes to the database... important: do not delete or change any temporary files now
```

get a list of all your entries, including login names:

```$ keys list -l```

copy to clipboard an entry including the word "gmail":

```
$ keys copy gmail
gmail/john@gmail.com copied, clearing clipboard in 20
```

## tips and tricks

display all your entries in a fancy way:

```keys list -lt | sed 1d | column -t```
