# Troubleshoot upgrades
This section contains some ideas for troubleshooting common problems experienced
with upgrading TimescaleDB.

<!---
* Keep this section in alphabetical order
* Use this format for writing troubleshooting sections:
 - Cause: What causes the problem?
 - Consequence: What does the user see when they hit this problem?
 - Fix/Workaround: What can the user do to fix or work around the problem? Provide a "Resolving" Procedure if required.
 - Result: When the user applies the fix, what is the result when the same action is applied?
* Copy this comment at the top of every troubleshooting page
-->

## Error updating TimescaleDB when using a third-party PostgreSQL admin tool
The update command `ALTER EXTENSION timescaledb UPDATE` must be the first command
executed upon connection to a database. Some admin tools execute commands before
this, which can disrupt the process. Try manually updating the database with
`psql`. For instructions, see the [updating guide][update].

[update]: /how-to-guides/update-timescaledb/#update-timescaledb
