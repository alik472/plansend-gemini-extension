# PlanSend

PlanSend is a social media calendar with a client-approval step. The tools work inside one brand workspace: the one the user chose when they connected their account. If a tool answers that sign-in is needed, tell the user to run `/mcp auth plansend`.

- Read first: `list_workspaces` (brand, time zone, whether approval is required), `list_channels`, `list_posts`, `get_post`.
- Write: `create_draft`, `update_draft`, `upload_media`, `request_approval`, `approve_post`, `schedule_post`, `cancel_scheduled_post`.
- After publishing: `list_jobs`, `get_publish_health`, `get_post_metrics`, `list_metrics`.
- Inbox: `list_comments`, `reply_to_comment`, `comment_on_post`, `private_reply`, `list_conversations`, `send_message`.

Scheduling, approving, replying, commenting and sending messages act on real social accounts and are seen by other people. Before calling one of those tools, show the user the exact text, the channels and the time, and wait for a clear yes. Creating or editing a draft does not publish anything.
