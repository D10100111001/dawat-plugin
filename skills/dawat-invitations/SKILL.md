---
name: dawat-invitations
description: Create or manage digital event invitations, invitation drafts, guest lists, and RSVPs with Dawat when the user asks for a wedding, nikkah, birthday, dinner, or party invitation. Use the connected Dawat MCP tools for persistent invitations and guest state.
---

# Dawat invitations

Turn the requested occasion into a saved invitation and return the relevant edit,
manage, or published link. Use only tools exposed by the connected account.

- Establish title, host, date/time with timezone, and venue from the conversation.
  Request only details that materially affect the invitation; do not invent dates,
  locations, recipients, or contact data.
- Use `list_templates` or `list_page_themes` to choose an available core design.
  Choose `card` for a formal keepsake or `page` for a casual gathering. Compose
  warm, concise invitation wording from the user's information.
- For a requested Signature design, check `list_signature_experiences` for an
  existing entitlement. Explain unavailable access without offering an upgrade,
  checkout, or purchase link. Use Standard core for unspecified requests.
- `create_invitation` saves a draft. Use `update_invitation` for edits. When the
  request is to review a draft, return its edit link and leave it unpublished.
- Publish only with explicit user intent. If the user already requested
  publication of the stated invitation, use that authorization without asking
  again. Otherwise show the saved details before seeking publication approval.
- Add only the guest list provided or specifically selected by the user. A guest
  without delivery contact information can still receive a personal share link.
  Do not invent an email address, scrape contacts, or add unrequested recipients.
- `send_invitations` contacts real people. Establish the invitation, exact audience,
  channel, message purpose, and explicit sending authorization first. Reuse clear
  authorization already given for that audience; do not expand it to reminders,
  additional recipients, or other channels. Report actual results and skipped
  guests, rather than claiming delivery from a successful request alone.
- URL import is optional service functionality. If extraction is unavailable,
  build a draft from user-provided details without claiming the page was imported.
- Use `list_my_invitations`, `get_invitation`, and the RSVP tools to read connected
  account state. Summarize counts and next actions; reveal guest contact details
  only when necessary for the user's requested task.
- Deleting invitations or guests can remove associated data permanently. Explain
  the exact effect and require specific deletion authorization before invoking
  the destructive tool. Publishing, deleting, and sending are separate intents.

First use requires connecting a Dawat account through OAuth. Tool results are
account-scoped. Links to the editor and guest manager support further refinement.
Do not request tokens in chat or put credentials in URLs.
