# fzf :heart: himalaya

An interactive mail client built on [himalaya](https://github.com/pimalaya/himalaya) and fzf.

## Requirements

- [himalaya](https://github.com/pimalaya/himalaya) v2, with at least one account configured
- [fzf](https://github.com/junegunn/fzf) 0.48 or later
- [jq](https://github.com/jqlang/jq)
- [html2text](https://github.com/Alir3z4/html2text), to render HTML-only messages

## Install

```bash
export PATH="$HOME/.bin/hif:$PATH"
```

## Usage

```bash
hif                    # Interactive menu
hif a                  # Browse accounts
hif m                  # Browse mailboxes
hif e [MAILBOX]        # Browse envelopes (default: inbox)
hif c                  # Compose a message
hif -a work e          # Use a specific account
```

| Env             | Description                              |
|-----------------|------------------------------------------|
| `HIF_ACCOUNT`   | Account to use (default account if unset) |
| `HIF_PAGE_SIZE` | Envelopes per page (default: 100)        |

Messages are viewed and composed in `$VISUAL` / `$EDITOR`.

### Keybindings

| Key      | Action                                    |
|----------|-------------------------------------------|
| `Enter`  | Drill down / view message                 |
| `Ctrl+P` | Toggle preview                            |
| `Ctrl+E` | Reply                                     |
| `Ctrl+N` | Compose                                   |
| `Ctrl+K` | Toggle read/unread                        |
| `Ctrl+S` | Toggle flagged                            |
| `Ctrl+O` | Move to mailbox                           |
| `Ctrl+X` | Delete (to trash)                         |
| `Ctrl+Q` | Search on server with the typed query     |
| `Ctrl+R` | Reload                                    |
| `Ctrl+A` | Switch account                            |
| `Tab`    | Multi-select                              |
| `Esc`    | Back                                      |

Server search uses himalaya's query language, e.g. `from alice and not flag seen`.
