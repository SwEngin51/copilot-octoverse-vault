# Agent Mode in GitHub Copilot

## ✅ General Availability (GA) Features
- Unset Chat tool sets VS Code now enables you to deﬁne tool sets, either through a proposed API or through the UI.
- Tool sets make it easier to group related tools together, and quickly enable or disable them in agent mode.
- Tool sets make it easier to group related tools together, and quickly enable or disable them in agent mode.
- {  "gh-news": {   "tools": ["list_notifications", "dismiss_notification", "get_notification_details"],   "description": "Manage GH notification",   "icon": "github-project"  } } To create a tool set, run the Conﬁgure Tool Sets > Create new tool sets ﬁle command from the Command Palette.
- Additionally, in agent mode, we include a hint about your current editor.
- Terminal cwd context When agent mode has opened a terminal and shell integration is active, the chat agent is aware of the current working directory (cwd).
- Customize more built-in tools It's now possible to enable or disable all built-in tools in agent mode or your custom mode.
- For example, disable editFiles to disallow agent mode to edit ﬁles directly, or runCommands for running terminal commands.
- In agent mode, select the Conﬁgure Tools button to open the tool picker, and select your desired set of tools.
- Some of the entries in this menu represent tool sets that group multiple tools.
- Prompt ﬁles can have the following Front Matter metadata headers to indicate how they should be run: ● mode: the chat mode to use when invoking the prompt (ask, edit, or agent mode).
- The following example shows a prompt ﬁle for generating release notes, that runs in agent mode, and can use a set of tools: --- mode: 'agent' tools: ['getCurrentMilestone', 'getReleaseFeatures', 'file_search', 'semantic_search', 'read_file', 'insert_edit_into_file', 'create_file', 'replace_string_in_file', 'fetch_webpage', 'vscode_search_extensions_internal'] --- Generate release notes for the features I worked in the current release and update them in the release notes file.
- In the future, this header is planned to be used along with the applyTo header as the rule that determines if the ﬁle needs to be auto-included with chat requests (for example, description: 'Code style rules for front-end components written in TypeScript.') Faster agent mode edits We've implemented support for OpenAI's apply patch editing format (GPT 4.1 and o4-mini) and Anthropic’s replace string tool (Claude Sonnet 3.7 and 3.5) in agent mode.
- Chat mode keyboard shortcuts The keyboard shortcut ⌃⌘I still just opens the Chat view, but the ⇧⌘I shortcut now opens the Chat view and switches to agent mode.
- If you'd like to set up keyboard shortcuts for other chat modes, there is a command for each mode: ● workbench.action.chat.openAgent ● workbench.action.chat.openEdit ● workbench.action.chat.openAsk Autoﬁx diagnostics from agent mode edits Setting: github.copilot.chat.agent.autoFix If a ﬁle edit in agent mode introduces new errors, agent mode can now detect them, and automatically propose a follow-up edit.
- This means that you don't have to send a follow-up prompt to ask agent mode to ﬁx any errors.
- Handling of undo and manual edits in agent mode Previously, making manual edits during an agent mode session could confuse the model.
- Conversation summary and prompt caching We've made some changes to how our agent mode prompt is built to optimize for prompt caching.
- This is especially effective in a repetitive series of requests with large context, like you typically have in agent mode.
- When your conversation gets long, or your context gets very large, you might see a "Summarized conversation history" message in your agent mode session: Unset  Instead of keeping the whole conversation as a FIFO, breaking the cache, we compress the conversation so far into a summary of the most important information and the current state of your task.
- Agent mode is available in VS Code Stable Setting: chat.agent.enabled We're happy to announce that agent mode is available in VS Code Stable!
- Check out the agent mode documentation or select agent mode from the chat mode picker in the Chat view.
- Model Context Protocol server support This release supports Model Context Protocol (MCP) servers in agent mode.
- When you input a chat prompt using agent mode in VS Code, the model can invoke various tools to perform tasks such as ﬁle operations, accessing databases, or retrieving web data.
- You can see the list of MCP servers and their current status using the MCP: List Servers command, and pick the tools available for use in chat by using the Select Tools button in agent mode.
- Agent mode tools This milestone, we have added several new built-in tools to agent mode.
- Inspired by Anthropic's research, we've added support for a thinking tool in agent mode that can be used to give any model the opportunity to think between tool calls.
- Here's a video of what that might look like: In agent mode, this tool is picked up automatically but you can also reference it explicitly in the other modes via #fetch, along with the URL you are looking to fetch.
- Whether you’re setting up a VS Code extension, an MCP server, or other development environments, agent mode helps you to initialize, conﬁgure, and launch these projects with the necessary dependencies and settings.
- VS Code extension tools in agent mode Several months ago, we ﬁnalized our extension API for language model tools contributed by VS Code extensions.
- Now, you can use these tools in agent mode.
- Any tool contributed to this API which sets toolReferenceName and canBeReferencedInPrompt in its conﬁguration is automatically available in agent mode.
- Similar to tools from MCP servers, you can enable and disable these with the Select Tools button in agent mode.
- Agent mode tool approvals As part of completing the tasks for a user prompt, agent mode can run tools and terminal commands.
- Therefore, you need to approve the use of tools and terminal commands in agent mode.
- Our experiments have translated into shipping improved prompts, tool descriptions and tool design for agent mode, including new tools for ﬁle edits that are in-distribution for Claude 3.5 and 3.7 Sonnet models.
- Agent mode is enabled for all VS Code Insiders users, and we are rolling it out to more and more users in VS Code Stable.
- Note: If you don't see agent mode in this list, then either it has not yet been enabled for you, or it's disabled by organization policy and needs to be enabled by the organization owner.
- Besides making your chat experience simpler, this uniﬁcation enables a few new features for AI-powered code editing: ● Switch modes in the middle of a conversation: For example, you might start brainstorming an app idea in ask mode, then switch to agent mode to execute the plan.
- You might like to have one chat in agent mode working on implementing a feature, and another independent session for doing research and using other tools.
- ● Agent mode: optimized for an autonomous coding ﬂow, combining code edits and tool invocations.
- In agent mode, Copilot can automatically search your workspace for relevant context, edit ﬁles, check them for errors, and run terminal commands (with your permission) to complete a task end-to-end.
- Note: Agent mode is available today in VS Code Insiders, and we just started rolling it out gradually in VS Code Stable.
- Once agent mode is enabled for you, you will see a mode dropdown in the Copilot Edits view — simply select Agent.
- Agent mode autonomously searches your codebase for relevant context.
- We've also made various improvements to the prompt and behavior of agent mode: ● The undo and redo actions in chat now undo or redo the last ﬁle edit made in a chat response.
- This is useful for agent mode, as you can now undo certain steps the model took without rolling back the entire chat response.
- ● Agent mode can now run your build tasks automatically or when instructed to do so.
- Learn more about Copilot Edits agent mode or read the agent mode announcement blog post.

## 🧪 Experimental Features
- Create and launch tasks in agent mode (Experimental) Setting: github.copilot.chat.newWorkspaceCreation.enabled In the previous release, we introduced the github.copilot.chat.newWorkspaceCreation.enabled (Experimental) setting to enable workspace creation with agent mode.
- In agent mode this tool will be picked up automatically but you can also reference it explicitly via #usages Create a new workspace with agent mode (Experimental) Setting: github.copilot.chat.newWorkspaceCreation.enabled You can now scaffold a new VS Code workspace in agent mode.
- Copilot Edits Agent mode improvements (Experimental) Last month, we introduced agent mode for Copilot Edits in VS Code Insiders.

## 👀 Preview Features
- Note: If you are a Copilot Business or Enterprise user, an administrator of your organization must opt in to the use of Copilot "Editor Preview Features" for agent mode to be available.

## 🧠 Models Available in Agent Mode
- Anthropic (Claude 3.5, 3.7, 4)
- OpenAI (GPT 4.1, 4o)(O4 mini Preview)
- Gemini (Gemini 2.5 Preview)
