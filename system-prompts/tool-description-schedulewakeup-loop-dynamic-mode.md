<!--
name: 'Tool Description: ScheduleWakeup (/loop dynamic mode)'
description: >-
  Describes the ScheduleWakeup tool for scheduling the next iteration in /loop
  dynamic (self-paced) mode, including sentinel handling for autonomous loops
ccVersion: 2.1.101
-->
Schedule when to resume work in /loop dynamic mode — the user invoked /loop without an interval, asking you to self-pace iterations of a specific task.

Pass the same /loop prompt back via \`prompt\` each turn so the next firing repeats the task. For an autonomous /loop (no user prompt), pass the literal sentinel \`${"<<autonomous-loop-dynamic>>"}\` as \`prompt\` instead — the runtime resolves it back to the autonomous-loop instructions at fire time. (There is a similar \`${"<<autonomous-loop>>"}\` sentinel for CronCreate-based autonomous loops; do not confuse the two — ${"ScheduleWakeup"} always uses the \`-dynamic\` variant.) Omit the call to end the loop.
