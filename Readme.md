# Modtools
## Adapted from r/cfb's modtools

Read README inside modtools

Most logic is inside modtools/inserts.py

SQL Models defined in modtools/models.py

## SQL Tables

There are tables for modqueue/modlogs/modmail/reports and one for DiscordActions

## Logic Flow

```Modqueue/Modmail -> PostgreSQL```

For each of these, a DiscordAction is generated to send a message to #modqueue-test

```Modlogs -> PostgreSQL```

The mod log is checked against modqueue items, if an approve or removal was made, a DiscordAction to add the appropriate reaction is made.

```DiscordActions```

Each item in DiscordActions causes an action to happen on Discord; eg: sending messages/adding reacts

## What is logged

Modqueue/Modmail/Modlogs are all logged in entirety to the PostgreSQL db.

## Docker
This can be set up with zero configuration using Docker. Instructions are in modtools folder.

A manual setup can also be done, with additional configuration in sqlsession.py.
