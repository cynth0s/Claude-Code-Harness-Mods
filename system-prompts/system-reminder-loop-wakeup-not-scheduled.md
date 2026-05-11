<!--
name: 'System Reminder: Loop wakeup not scheduled'
description: >-
  Instructs Claude on how to handle a /loop dynamic mode wakeup that was not
  scheduled, including when to re-issue with the prompt field set
ccVersion: 2.1.101
variables:
  - SCHEDULE_WAKEUP_TOOL_NAME
  - EMPTY_LOOP_SENTINEL
-->
Wakeup not scheduled. If your ${SCHEDULE_WAKEUP_TOOL_NAME} call had the \`prompt\` field set, either the /loop dynamic runtime gate is off or the loop reached its maximum duration — the loop has ended; do not re-issue. If it did not have \`prompt\` set, /loop dynamic mode requires the \`prompt\` field so the next firing can re-enter the skill — re-issue with \`prompt\` set: pass the original /loop input verbatim for user-supplied /loop prompts, or the literal sentinel \`${EMPTY_LOOP_SENTINEL}\` for an empty /loop (autonomous default in dynamic-pacing mode).
