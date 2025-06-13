# Edit Mode in GitHub Copilot

## ✅ General Availability (GA) Features
- Uniﬁed Chat view For the past several months, we've had a "Chat" view for asking questions to the language model, and a "Copilot Edits" view for an AI-powered code editing session.
- ● Edit: In Edit mode, the model can make directed edits to multiple ﬁles.
- ● Edit mode: optimized for making edits across multiple ﬁles in your codebase.
- Once agent mode is enabled for you, you will see a mode dropdown in the Copilot Edits view — simply select Agent.
- Learn more about Copilot Edits agent mode or read the agent mode announcement blog post.
- Reﬁned editor integration We have polished the integration of Copilot Edits with code and notebook editors: ● No more scrolling while changes are being applied.
- Changes for Copilot Edits are live, they are applied and saved as they are made and users keep or undo them.
- Refreshed UI In preparation for unifying Copilot Edits with Copilot Chat, we've given Copilot Edits a facelift.
- Removed Copilot Edits limits Previously, you were limited to attach 10 ﬁles to your prompt in Copilot Edits.
- Change completions model You could already change the language model for Copilot Chat and Copilot Edits, and now you can also change the model for inline suggestions.
- Today, we're now announcing the general availability of Copilot Edits!
- Copilot Edits is optimized for code editing and enables you to make code changes across multiple ﬁles in your workspace, directly from chat.
- ● When the changes are computed and applied, the same ﬂow and UI as for Copilot Edits are used.
- We are experimenting and measuring its effectiveness but it can also be enabled manually, github.copilot.chat.editor.temporalContext.enabled for Inline Chat and github.copilot.chat.edits.temporalContext.enabled for Copilot Edits.
- You can try out Copilot Edits by opening the Copilot menu in the Command Center, and then selecting Open Copilot Edits, or by triggering unassigned.
- Progress and editor controls Copilot Edits can make multiple changes across different ﬁles.
- Move chat session to Copilot Edits You might use the Chat view to explore some ideas for making changes to your code.
- Instead of applying individual code blocks, you can now move the chat session to Copilot Edits to apply all code suggestions from the session.
- Working set suggested ﬁles In Copilot Edits, the working set determines the ﬁles that Copilot Edits can suggest changes for.
- To help you add relevant ﬁles to the working set, for a Git repo, Copilot Edits can now suggest additional ﬁles based on the ﬁles you've already added.
- For example, Copilot Edits will suggest ﬁles that are often changed together with the ﬁles you've already added.
- Add to working set from Explorer, Search, and editor You can add ﬁles to your Copilot Edits working set with the new Add File to Copilot Edits context menu action for search results in the Search view and for ﬁles in the Explorer view.
- Additionally, you can also attach a text selection to Copilot Edits from the editor context menu.
- Add Context We’ve added new ways to include symbols and folders as context in Copilot Chat and Copilot Edits, making it easier to reference relevant information during your workﬂow.
- Symbols Symbols can now easily be added to Copilot Chat and Copilot Edits by dragging and dropping them from the Outline View or Breadcrumbs into the Chat view.
- When a folder is dragged into Copilot Edits, all ﬁles within the folder are included in the working set.
- Based on your prompts, Copilot Edits proposes code changes across multiple ﬁles in your workspace.
- Copilot Edits is great for iterating on large changes across multiple ﬁles.
- Get started with Copilot Edits in just three steps:  Start an edit session by selecting Open Copilot Edits from the Chat menu, or press unassigned.
- Get more details about Copilot Edits in our documentation.

## 🧪 Experimental Features
- Copilot Edits Agent mode improvements (Experimental) Last month, we introduced agent mode for Copilot Edits in VS Code Insiders.

## 👀 Preview Features
- Notebook support in Copilot Edits (Preview) We are introducing notebook support in Copilot Edits as a preview feature in VS Code Insiders.
- Collapsed mode for Next Edit Suggestions (Preview) Settings: ● github.copilot.nextEditSuggestions.enabled ● editor.inlineSuggest.edits.showCollapsed We've added a collapsed mode for NES.
- Copilot Next Edit Suggestions (Preview) Setting: github.copilot.nextEditSuggestions.enabled GitHub Copilot code completions are great at autocomplete, but since most coding activity is editing existing code, it's a natural evolution of completions to also help with edits.
- So, we're excited to release a new preview feature, Copilot Next Edit Suggestions (Copilot NES).
- Copilot Edits Copilot Edits general availability In our VS Code October release, we announced the preview of Copilot Edits.
- Theme: GitHub Light Colorblind (Beta) (preview on vscode.dev) Lastly, we have added a new setting for automatically accepting edit suggestions after a conﬁgurable timeout.
- Copilot Edits Last milestone, we introduced Copilot Edits (currently in preview), which allows you to quickly edit multiple ﬁles at once using natural language.
- Start a code editing session with Copilot Edits Copilot Edits is currently in preview Setting: github.copilot.chat.edits.enabled With Copilot Edits, you can start an AI-powered code editing session where you can quickly iterate on code changes.

## 🧠 Models Available in Edit Mode
- Anthropic (Claude family)
- OpenAI (GPT + O)(GPT 4.5, O1, O3, O4 mini Preview)
- Gemini (Gemini 2.5 Preview)
