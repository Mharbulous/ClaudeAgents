Command Name: /your_command_name
This is a template for creating a custom command in Claude Code.  Created September 1, 2025

Instructions:

Save this file with a .md extension inside your .claude/commands/ directory.

The filename (e.g., refactor.md) will become the command name (/refactor).

Replace the content below with the prompt you want to use for your command.

PROMPT CONTENT: Best Practices

<instruction>
You are an expert software engineer. Your task is to perform a specific action based on the user's request.
</instruction>

<task>
Describe the single, focused task you want Claude to perform here.
</task>

<context>
Provide any necessary context for the task. This can include:

Code style guidelines (e.g., "Use ES modules, not CommonJS.")

Project architecture overview (e.g., "The main logic is in src/services/main_service.py.")

Specific files to reference (e.g., "Review the utils.js file for helper functions.")
</context>

<example>
Provide a concrete example of the desired input and output to guide Claude.
</example>

Using Arguments

You can use the $ARGUMENTS variable to pass in values from the chat. The example below shows how you can instruct Claude to take the filename as an argument.

<task>
Refactor the code located at the file path: `$ARGUMENTS`.
</task>

<instruction>
Your goal is to improve readability and performance. Add clear, concise comments to explain complex logic.
</instruction>

How to Use:
Simply type /your_command_name in the chat to run this prompt. If your prompt uses $ARGUMENTS, type /your_command_name <your_argument>.