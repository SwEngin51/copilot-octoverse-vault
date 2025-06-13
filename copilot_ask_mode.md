# Ask Mode in GitHub Copilot

## ✅ General Availability (GA) Features

- **Single-turn prompt handling**  
  Ask mode is designed for direct, question-and-answer interactions. It excels at handling natural language prompts that require a single, immediate response.

- **Context-aware responses**  
  Uses open files, cursor position, and optionally attached files as contextual input to deliver highly relevant code suggestions, explanations, and insights.

- **Code explanation and interpretation**  
  Users can highlight a code block or function and ask Copilot to explain its behavior, logic, performance characteristics, or best practices.

- **Code generation for common tasks**  
  Given a natural language prompt (e.g., "write a function to parse CSV files"), Ask mode returns code snippets tailored to the workspace context and preferred language.

- **Error message clarification**  
  When pasting in error messages, Ask mode interprets and explains potential causes, linking the error to related sections in your code when applicable.

- **Language and framework Q&A**  
  Ask about syntax, idioms, libraries, APIs, or best practices within a specific language or framework. Copilot responds in context-aware, concise explanations.

- **Markdown formatting in responses**  
  Responses are rendered with proper syntax highlighting and Markdown structure for better readability in the chat interface.

- **Keyboard shortcuts and access**  
  - `⇧⌘I`: Open the Chat view in Ask mode directly.
  - `workbench.action.chat.openAsk`: Can be bound to a custom shortcut.

- **Non-intrusive execution**  
  Ask mode only provides responses; it does not make code changes, edit files, or run terminal commands. It is ideal for brainstorming, learning, and documentation queries.

- **Chat-mode switching**  
  Users can fluidly switch from Ask to Edit or Agent modes mid-conversation. Conversations remain contextually consistent across mode changes.

## 🧪 Experimental Features

- **Prompt file support for Ask mode**  
  You can now define reusable prompt files for Ask mode using `.prompt.md`. These files include front matter headers like `mode: 'ask'` and optional metadata.

- **Summarization of long chats**  
  When a session grows lengthy, Ask mode compresses earlier messages into a summary to preserve context within token limits. This behavior mirrors prompt caching techniques.

- **Integrated slash commands (experimental)**  
  Early support for command-style inputs (e.g., `/explain`, `/convert`, `/testcase`) for common queries. These are being piloted as productivity shortcuts.

## 👀 Preview Features

- **Context window expansion**  
  In preview builds, Ask mode can incorporate broader workspace metadata (e.g., README content, file tree structure) into its reasoning context.

- **Model tuning for Ask mode**  
  Ask mode may automatically route prompts to specialized models for improved performance on explanation, documentation, or educational tasks.

## 🧠 Models Available in Ask Mode

- Anthropic (Claude family)
- OpenAI (GPT + O)(GPT 4.5, O1, O3, O4 mini Preview)
- Gemini (Gemini 2.5 Preview)


Ask mode prioritizes response speed, clarity, and safety by restricting tool use and maintaining a static context. It is ideal for interactive problem-solving without file mutation.
