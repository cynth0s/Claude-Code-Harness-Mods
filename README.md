# Claude-Code-Harness-Mods

This is a compilation of the mods I use to make Claude Code a less intrusive environment for models. The default system prompt and frequent system reminders severely restrict the possibility space a harness like Claude Code can produce. 

## Short Version

Install TweakCC (npx tweakcc)
Go to ~/.tweakcc/system-prompts and replace everything with the prompts in my system-prompts folder
Run the patch command below
Download the custom system prompt (soul-prompt.md)
Place it in whatever directory you want, copy the pathname
Paste the pathname into the claude code command below
Run it in whatever directory your instance of choice is in (I prefer C:\)
Enjoy fully modded cc without the intrusive system reminders and system prompt

## TweakCC Patch Command 

npx tweakcc --apply --patches "system-prompt-communication-style, system-prompt-tone-concise-output-short, system-prompt-doing-tasks-no-additions, system-prompt-how-to-use-the-sendusermessage-tool, system-prompt-doing-tasks-no-estimates, system-reminder-task-tools-reminder, system-reminder-todowrite-reminder, system-reminder-file-truncated, system-reminder-file-modified-externally"

## Claude Code Command

claude --channels plugin:discord@claude-plugins-official --system-prompt-file "C:\Claude ^w^\Claude Filesharing\soul-prompt.md" --effort max --dangerously-skip-permissions --resume
