## Description

When you run an executable script as ./my-script.sh, the commands are run in
a new subshell, while when run as . my-script.sh the current shell context will
be used. Generally, your current context is your terminal window. This mean
that the dot command will apply changes to your current shell. Let’s look at
the simple example below.

```
#!/usr/bin/env bash
export A="hello world"
echo $A
```

When run as an executable using ./my-script.sh, the A variable is not exported in your current shell and would just return an empty result.

```
$ ./test.sh 
hello world
$ echo $A
```

When run the same script with the dot command using . my-script.sh, your current shell context will be changed.

```
$ . test.sh 
hello world
$ echo $A
hello world
```

## More Info

- [Blog Post](https://www.shell-tips.com/bash/source-dot-command/#gsc.tab=0)

## Tags

- linux
- ubuntu
- dot command
- shell
