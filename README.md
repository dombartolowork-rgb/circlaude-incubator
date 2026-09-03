# Cir'Claude, Windows install test build

**This is a throwaway.** It exists to answer one question: does Cir'Claude
install and sign in on a Circle Windows laptop?

The client-specific parts have been stripped out, so it is deliberately less
useful than the real thing: the project code map is a template, and the
SharePoint and Teamwork ids are not here. The real version is private, and
will live on Circle's own Azure DevOps.

## What you need first

Raise these with IT as **one** request:

1. **Claude Code**, which runs inside the Claude desktop app
2. **Git**
3. **Python 3** (`winget install Python.Python.3.12`, per-user, no admin)

## Install

In Claude Code:

```
/plugin marketplace add https://github.com/<this repo>
/plugin install circlaude@circlaude
```

Then:

```
/circlaude:onboard
```

That signs you in to Microsoft with **your own** account, using a device code
in your browser. Nothing is shared and nobody else can read your mail
through it.

## What we need to know

- did it install at all
- does `circle whoami` show you signed in
- does `circle inbox --limit 5` print anything
- anything that errors, with the error text, however small

That is the whole test. Report back to Dom
(dom.bartolo@circleagency.co.uk) and then you can remove it:

```
/plugin uninstall circlaude
```

## Safety, unchanged from the real build

Email cannot be sent without you confirming it, and that is in the code, not
a setting. Time logging is a dry run by default and posts nothing without an
explicit go.
