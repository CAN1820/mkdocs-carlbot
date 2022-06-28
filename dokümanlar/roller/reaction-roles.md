# Reaction Roles

!!! tip
    Deleted messages are also cleared from the database. Pin the reaction role message to make it immune to purging.

### RR Management

!!! info
	`reactrole`, `reactionrole`, and `rr` are all aliases for the same base command.

???+ tldr "RR Management"

	| Name | Example | Usage |
	| :--- | :--- | :--- |
	| **rr [make\|setup]** | !rr make | Starts the interactive setup to get you started with reaction roles |
	| **rr [| !rr clearwl 458641514017587210  | Removes all roles from your whitelist for that set of reaction roles. |
	| **rr selfdestruct &lt;msg\_id&gt; &lt;time&gt;** | !rr selfdestruct 458641514017587210 7d | Deletes the message and all of its reaction roles after the time is up. |
	| **rr edit &lt;msg\_id&gt; &lt;title \| description&gt;** | !rr edit 458641514017587210 Games \| Click on the games you want to be notified by | Edits the title and description, works like it does in the make command |
	| **rr [channel\|cc] [name=get-roles]** | !rr cc color-roles | Creates a channel with the sort of permissions you most likely want for a reaction role channel (yes, add reactions is off, this is intentional) |
	| **rr fix** | !rr fix | Accidentally (or intentionally) cleared all reactions? Use this command to have the bot add the reactions missing |

### RR Types

!!! info
    Types are per message and change their behavior. Every message has a type which defaults to normal.

???+ tldr "RR Behavioral Types"

	| Name | Example | Usage |
	| :--- | :--- | :--- |
	| **rr unique &lt;msg\_id&gt;** | !rr unique 458641514017587210 | Marks a message as 'unique' meaning a member can only claim one role from this message at a time, this works per message. Automatically removes the old reactions for you |
	| **rr binding &lt;msg\_id&gt;** | !rr binding 458641514017587210 | A combination of rr verify and rr unique. Allowing for members to limit people to one choice ever. |
	| **rr link &lt;base\_id&gt; &lt;target\_id&gt;** | !rr link 458641514017587210 445066811097219082 | By linking two or more messages together, only one role from either message can be self-assigned. If you have 30 color roles for instance, linking the two messages together (since the limit is 20/message) allows a smooth, user-friendly experience when picking up roles. |
	| **rr unlink &lt;msg\_id&gt;** | !color&gt; &lt;title \| description&gt; &lt;emoji&gt; &lt;role&gt;** | -- | Works like **!rr aio** but also marks the message as unique |
	| **rr aiov &lt;channel&gt; &lt;color&gt; &lt;title \| description&gt; &lt;emoji&gt; &lt;role&gt;** | -- | All in one command to create a verification reaction role. |
	| **rr aioi &lt;channel&gt; &; &lt;title \| description&gt; &lt;emoji&gt; &lt;role&gt;** | -- | All in one command to create an inverse verification reaction role, i.e. one that only removes roles. |
	| **!rr fixforeign &lt;msg\_id&gt;** | !rr fixforeign 458641514017587210 | Super niche command which can be used to have the bot react to emojis the bot doesn't have access to. One reason you might want to use this is because you want to use google's blob emojis. This command isn't required for these emojis to work, it only makes it so that the bot has its reactions added to the message. **YOU HAVE TO REACT TO THE MESSAGE WITH THE EMOJIS YOURSELF BEFORE USING THIS COMMAND** |
	| **rr maxroles &lt;msg\_id&gt; [&lt;role&gt; &lt;number&gt;...]** | !rr maxroles 458641514017587210 DPS 10 | Want to limit the number of x role? With this, you can. **NOTE** This checks for how many people have the role, not how many reactions there are. |
	| **rr [colour\|color] &lt;msg\_id&gt; &lt;color&gt;** | !rr color 458641514017587210 \#00ee28 | Changes the accent color of the specified  bot message |

[The fastest and most reliable unique reaction roles of any bot.](https://i.imgur.com/A7ShLfZ.mp4)

![Me setting up reaction roles in my support server.](../images/reaction_role_setup.png)
