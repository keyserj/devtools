
# Helpful practices to remain organized
Everyone's workflow is a bit different, but here are some things I do to keep organized with my developing/reviewing/communicating. These are much more opinionated than the general dev tools.

## Email

### 3 categories of emails
* Unread => still need to read
* Read => still need to address (e.g. PR request, archive after reviewed)
* else => archived
Mostly < 10 emails in inbox, because an email is basically a TODO. It's easier to keep track of emails if you don't have to scroll to see them all.

## Slack

### Minimal DM usage
_only_ use DM's if you know you won't have to bring someone else into the conversation. This prevents loss of context/efforts spent reconveying context.
This is easy if you accept that it's ok to create channels liberally. Everyone's got the power! Channel examples that help take conversations out of DM's:
* channel per epic (esp helpful if stakeholders are outside of team, or if epic affects other teams)
* channel per initiative
* internal channel for team
* external channel for team - intended for other people to ask q's to the team

### Unstar & hide DM's/channels that you expect not to use today
Pretty much at all times, I've got starred
* #dev/#dev-support/#tnt
* DM's with teammates
All other channels/DM's, I'll star when a conversation pops up so they're easy to go back to, then unstar when the conversation is over. This helps because a starred channel/DM implies there may be a TODO to check up on. I know when it's time to prune if I have to scroll to see all my starred channels/DM's.

### Mute channels that you want to participate in, but aren't important enough to distract you
This basically just helps make Slack notifications more valuable. I'll check these whenever I have a break in my flow. Examples for me: #post-deploy, #random, #nonprod-deployments.

## Named terminal window per workstream, with splits
Use tmux, wonder if this works with iTerm
* Almost always need multiple terminals per workstream, hence splits; e.g. 1. local rails console 2. local rails server 3. rails repo 4. SIT rails console
* Usually have one window for running processes not specific to a workstream (lac/vault/ui/flik)

## TODO list
Sometimes I have a lot of things to do that don't justify tickets (things from emails, slack conversations, etc), but take longer than a couple minutes each, so it'd be helpful to put them in a list to prioritize them. When this is the case, I group them all into a TODO list.
I just have one big file for these that's always open. It's only relevant if I have TODO's for the current day. I also use "WAIT" and "DONE" items - "DONE" to keep the item in history, "WAIT" to indicate that I should check back on the item.
