# Modtools
## Adapted from r/cfb's modtools

Read README inside modtools

Most logic is inside modtools/inserts.py

SQL Models defined in modtools/models.py

## Logic Flow

```Modqueue/Modmail -> PostgreSQL```

For each of these, a DiscordAction is generated to send a message to #modqueue-test

```Modlogs -> PostgreSQL```

The mod log is checked against modqueue items, if an approve or removal was made, a DiscordAction to add the appropriate reaction is made.

```DiscordActions```
Each item in DiscordActions causes an action to happen on Discord; eg: sending messages/adding reacts

## What is logged

Modqueue/Modmail/Modlogs are all logged in entirety to the PostgreSQL db.
