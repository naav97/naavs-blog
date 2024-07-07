+++
title = 'How to see the MySQL log'
date = 2024-07-07T17:37:39-05:00
draft = false
tags = ['MySQL']
+++
**WARNING**: Most of the information in this post was created by the free tier of CharGPT in 2024

This guide will be focused on Ubuntu, for other systems instructions may be similar.

## Find your _my.cnf_ file

Depending on the system and MySQL version, etc. The _my.cnf_ file may be in different places. Some common places to search for are:

* /etc/mysql/my.cnf
* /etc/my.cnf

If you don't find the config file in those places, you can try the following:

```Bash
sudo find -name my.cnf /
```

The file may be called my.ini

## Check the configuration

Ones you are in the config file, look for these two settings:

### general_log

This setting needs to be "ON"

### general_log_file

This setting will tell you where MySQL is saving the logs. The value should be an absolute path to a file.
