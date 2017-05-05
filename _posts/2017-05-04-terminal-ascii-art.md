---
title:  "Terminal Ascii Art"
tags: [code]
---

Decided to spice up my terminal with the golang gopher. <img alt="golang" src="{{ site.url }}/assets/images/terminal-ascii-art/golang.png" width="100px"/>


# Steps

## 1. Create ascii art

Leverage [this wonderful site](http://www.text-image.com/convert/ascii.html)
to convert an image to ascii art.

I put the resulting [golang.txt]({{ site.url }}/assets/images/terminal-ascii-art/golang.txt) file at `~/Pictures/golang.txt`

## 2. Edit `~/.bash_profile`

Write a script in `~/.bash_profile` to read `~/Pictures/golang.txt`
and `echo` its contents.

```sh
# golang ascii art
IFS=''
cat Pictures/golang.txt |
while read -r line
do
  echo "$line"
done
```

# Result

![terminal]({{ site.url }}/assets/images/terminal-ascii-art/terminal.png)

Worth it.
