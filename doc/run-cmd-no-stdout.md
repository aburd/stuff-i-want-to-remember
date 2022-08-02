## Description

You can prevent commands from printing to stdout by redirecting to input to
/dev/null.

I.E.
```
#! /usr/bin/fish
if which ls &> /dev/null
  echo "You have ls"
end
```

## More Info

na

## Tags

- shell
