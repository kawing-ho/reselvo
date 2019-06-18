# reselvo
Because 'resolve' is too mainstream


## What it does

It takes in a list of subdomians and resolves the heck out of them, saving the results to a specified directory of choice. 

It can perform in two ways:  
- As a one-off tool
- As a long-running daemon process :clock10:

Scanning the whole range of ports is also an option (will be included as a flag in arguments). Obviously this will take a lot longer so do it at your own leisure.

## One-off

Will provide estimation of the process (can take awhile especially with port-scanning turned on)

## Daemon

As a daemon it will run once per day and store the results
- File cleanup will be done by removing duplicates if the direcotry size is too large
- It will compare the current state versus previous state
- If any new changes occur, it can then alert you via Webhook (Slack) or Twilio SMS

# Installation 

```
pip install -r requirements.txt
```

A configuration file is present to allow for quick and presistent configs (instead of envvars)  
