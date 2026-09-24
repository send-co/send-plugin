---
name: saving-notes-with-send
description: Save what someone is working on to Send so they can pick it up in any AI. Use when they ask to save, remember or note something, keep context for later, hand work off to another AI app or a teammate, or pick up where they left off.
---

# Saving notes with Send

Send keeps notes in the person's Send workspace, outside this chat. Any official AI app they've authorized to Send can read them back, and so can their teammates. A note saved here in Claude can be picked up tomorrow in ChatGPT, Cursor or another Claude session.

## When to use it

Use Send notes when the person:

- says "save this", "remember this", "make a note" or "keep this for later"
- wants to stop now and continue later, here or in another AI app
- wants to hand context to a teammate or another agent
- asks what they decided, saved or worked on before
- says "pick up where I left off" or refers to earlier work you cannot see

Do not use notes for code, config or files that belong in the repository.


## Saving

1. `SaveNote` with a short plain title and a Markdown body. Write it so a
   reader with no access to this chat can act on it: the goal, the decisions,
   what is done, what is next.
2. Confirm the save only after the tool returns. Give the title back.

If a note on the same subject already exists, change it with `UpdateNote`
instead of saving a second copy. Use `DeleteNote` only when the person asks to
remove or forget a note.

## Picking up

1. `GetNotes` with a `query` that names the subject. Use the date and author
   filters for "yesterday" or "what my teammate saved".
2. Read the full note before you act on it or change it. Snippets leave out
   the revision that `UpdateNote` needs.
3. Tell the person which note you loaded, then continue the work.

## Publishing a note

When the person needs a link for someone outside the workspace, turn the note
into a page with the `creating-sites-with-send` skill.
