# Teamwork project codes

**This is a template.** The live code map is deliberately not in this
repository. Ask Dom for it, or build your own as you go.

Ids are point-in-time, so **reconfirm before committing time**:
`circle tw-projects "<code or stem>"`.

## How the codes work

Client prefixes are a few letters plus a sequential number, e.g. `ABC123`.
A code only resolves for time logging if an **active** Teamwork project's
name contains it, which is why `circle tw-log` can report NO PROJECT MATCH
for a code that exists in the Project Tracker.

Searching a stem returns the whole family in one call, so
`circle tw-projects "ABC11"` finds ABC110 through ABC119.

## Internal time

Internal work books to the non-billable project with `billable: false`, and to
a **task inside** it rather than the bare project. `circle tw-tasks` lists the
tasks. Put your own site's project id in `~/.circle/config.json`.

## Traps worth writing down as you find them

- Some jobs carry **two** codes, typically one for budget and sourcing and one
  for delivery. Booking to the wrong one is the most common mistake.
- Clients sometimes use an internal codename for a project that differs from
  the name on the job, and activations often sit inside a parent job's code
  rather than having their own.
- Campaign names frequently differ from job names, so searching SharePoint for
  the campaign is a reliable way to find the code.

Keep your own version of this file, per client, as you learn them.
