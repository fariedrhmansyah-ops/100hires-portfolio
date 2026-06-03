# 100Hires Portfolio Project — Setup Log

## Tools Installed

- **Cursor IDE** — Downloaded and installed from cursor.com. First time using it, but the interface felt familiar since it's based on VS Code.
- **Claude Code (VS Code extension)** — Installed inside Cursor via the Extensions panel. This is the official extension by Anthropic.
- **Codex (OpenAI extension)** — Also installed via the Extensions panel inside Cursor.

## Steps I Completed

1. Downloaded Cursor from cursor.com and installed it on Windows
2. Opened the Extensions panel with Ctrl+Shift+X, searched "Claude Code", and installed the Anthropic one (the one with 20M+ installs)
3. Did the same for "Codex" — found the OpenAI one and installed it
4. Tried to run the Claude Code CLI by typing `claude` in the terminal — got an error saying the command wasn't recognized
5. Looked it up and found I needed to install it separately via npm: `npm install -g @anthropic-ai/claude-code`
6. That also failed at first — different error this time
7. Created this GitHub repo and wrote up everything here

## Problems I Hit (and How I Figured Them Out)

**Problem 1: `claude` command not found in terminal**  
After installing the VS Code extension, I typed `claude` in the terminal and got a "not recognized" error. I didn't realize the CLI was a separate install from the extension.  
**Fix:** Searched the error online, found that I needed Node.js and npm first. Downloaded Node.js LTS from nodejs.org, installed it, then ran `npm install -g @anthropic-ai/claude-code`.

**Problem 2: npm itself was blocked by PowerShell**  
Even after installing Node.js, npm threw a `PSSecurityException` — something about scripts being disabled on the system.  
**Fix:** Found the fix on Stack Overflow. Ran `Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned` in PowerShell, then npm worked fine.

**Problem 3: Claude Code needs a Pro or Max subscription to log in**  
Once the CLI was working and I tried to authenticate, the browser opened and showed "Claude Max or Pro is required." I'm on the Free Plan.  
**Fix:** No workaround for now without upgrading or using an API key. I noted it and moved on. The extension is installed and ready — just needs credentials.

**Problem 4: Codex also needs a paid ChatGPT subscription**  
Same situation — the extension installed fine but login requires ChatGPT Plus or higher.  
**Fix:** Same as above, documented and moved forward.

## Honest Reflection

Most of the time on this wasn't spent installing things — it was spent figuring out why things weren't working. The PowerShell security error was the most annoying one because it wasn't obvious at first. Looking back, none of the problems were that hard once I actually read the error messages carefully and searched for them. That felt like a good sign.
