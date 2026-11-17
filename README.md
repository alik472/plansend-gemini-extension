# PlanSend for Gemini CLI

Work on your social media calendar from Gemini CLI. [PlanSend](https://plansend.io) is a social media calendar with a client-approval step: see what is drafted, waiting for approval, scheduled or published, write new drafts, send them to a client for review and schedule them to your connected channels.

## Install

```bash
gemini extensions install https://github.com/alik472/plansend-gemini-extension
```

## Sign in

PlanSend works in your own PlanSend account. Start Gemini CLI and run:

```
/mcp auth plansend
```

Your browser opens plansend.io, you sign in and approve the connection, and the CLI keeps the token on your computer. Run the same command again if the connection expires. You choose one brand workspace when you approve; the tools work inside that brand only.

## What you can ask

- Show my PlanSend posts and the status of each one.
- Draft a post for my channels about our autumn menu.
- Send my latest draft for client approval and give me the review link.
- Did yesterday's scheduled posts publish, and how did they perform?

## Tools

| Tool | What it does |
| --- | --- |
| `list_workspaces`, `list_channels` | The connected brand, its time zone and its social channels. |
| `list_posts`, `get_post` | Drafts, posts waiting for approval, scheduled and published posts. |
| `create_draft`, `update_draft` | Write and edit drafts. |
| `list_media`, `upload_media` | Images and video for posts. |
| `request_approval`, `approve_post` | Send a draft to a client with a private review link, and approve it. |
| `schedule_post`, `cancel_scheduled_post` | Schedule a post to its channels, or take it off the schedule. |
| `list_jobs`, `get_publish_health` | Whether scheduled posts went out. |
| `get_post_metrics`, `list_metrics` | How published posts performed. |
| `list_comments`, `reply_to_comment`, `comment_on_post`, `private_reply` | Read and answer comments. |
| `list_conversations`, `send_message` | Read and answer direct messages. |
| `ai_assist`, `ai_credits` | PlanSend's own writing help and the credits left for it. |

## Good to know

- You need a PlanSend account with at least one connected channel.
- Scheduling, approving, replying and sending messages act on your real social accounts. The extension tells Gemini to show you the text, channels and time and to ask before it does any of these.
- Owners and editors can write; reviewers can only read.

## Other MCP clients

The extension only points Gemini CLI at PlanSend's hosted MCP server (streamable HTTP):

```
https://plansend.io/mcp
```

Any MCP client that supports remote servers can use the same address. It signs you in with OAuth.

## Links

[Website](https://plansend.io) · [Privacy](https://plansend.io/privacy) · [Terms](https://plansend.io/terms) · [Help](https://plansend.io/help)

## License

The files in this repository are released under the MIT License. The PlanSend service itself is covered by its terms.
