# git2skype
Send your git commits to skype group chats

The [SkPy](https://github.com/Terrance/SkPy) Project provides a neat little python SDK around the skype messaging API. 

Using this API, its quite simple to create a small bot that sends your
development groups commits to your favourite Skype group.  Even tho it is 2021, there are
still people around that may stick to old fashioned
messaging services. .. ;)

The Example provided in this repository is a small bot that sends the latest
commits created to a repository to the configured Skype group, replaces ticket numbers with
urls and tries to be friendly ;)

# HOWTO

1) Logon to Skype and create a new group chat. Set the group chat title, add
the Skype account used for the bot aswell as other persons to the group. Be
sure to Logon with the Skype bot account once to accept the invitation.
3) Checkout this repository
2) Install required components (on the system that is serving the git
repositories).

```
pip3 install skpy
```
4) Edit the example script and set the required values for the
username/password/group title
5) On the node that serves the git repositories configure a post-receive hook
by copying the script to:

```
$GITDIR/hooks/post-receive
```

(or consider creating a symlink, dont forget to set the executable flag)

6) Push your changes and watch the bot reporting, like so:

![screenshot](skypebot.jpg?raw=true "Thebot")
