---
layout: post
title: The Tutorial of Fuzzing Network Daemon Using AFL
---
Recently, I have learned about how to use afl to fuzz network daemon, here i want to leave something that I wether I want to see it i can find it.

#Prepare AFL
```
# git clone https://github.com/mirrorer/afl.git
# cd afl
# make && make install
```

#Fuzz with AFL

-compile the target program with afl-gcc (use afl-g++ if is cpp)
```
CC=afl-gcc
```

-fuzz with afl
```
afl-fuzz -i in -o out target [args] [@@] (if the target program use file as input then use @@)
```


