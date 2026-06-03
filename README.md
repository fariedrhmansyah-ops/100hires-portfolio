# 100Hires Portfolio Project — Setup Log

## Tools Installed

- **Cursor IDE** — Downloaded from cursor.com and installed on Windows.
- **Claude Code for VS Code extension** — Installed via Cursor's Extensions panel (Ctrl+Shift+X). Found and installed the official extension by Anthropic.
- **Codex extension** — Installed via Cursor's Extensions panel. Found the official OpenAI Codex extension and installed it successfully.

## Steps Completed

1. Installed Cursor IDE from cursor.com
2. Opened the Extensions panel (Ctrl+Shift+X) and searched for "Claude Code" — installed the Anthropic extension
3. Searched for "Codex" — installed the OpenAI Codex extension
4. Attempted to log in to Claude Code CLI by running `npm install -g @anthropic-ai/claude-code` in the terminal
5. Created a public GitHub repository named `100hires-portfolio`
6. Edited this README.md file to document the setup process

## Issues Encountered & How I Solved Them

**Issue 1: PowerShell script execution was blocked**  
When running `npm install -g @anthropic-ai/claude-code`, I got a SecurityError saying running scripts is disabled on this system.  
**Solution:** I ran `Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned` in PowerShell, which resolved the restriction and allowed npm to run.

**Issue 2: Claude Code requires a Pro or Max subscription**  
After successfully installing the CLI, the login page showed "Claude Max or Pro is required to connect to Claude Code." My account is on the Free Plan.  
**Solution:** I documented this limitation. Claude Code can alternatively be used via an Anthropic API key. I proceeded with the remaining setup steps.

**Issue 3: Codex requires a ChatGPT Plus or Pro subscription**  
Similarly, Codex is only available to paid ChatGPT subscribers.  
**Solution:** Documented as a known limitation. Both tools are installed and ready to use once a subscription is available.

## Notes

This was my first time using Cursor IDE. The interface was familiar because it is built on VS Code. I learned how to fix PowerShell execution policy restrictions independently by researching the error message. All tools are installed and the setup process is fully documented.
