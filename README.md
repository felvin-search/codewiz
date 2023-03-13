<h1 align="center">

<img src="./images/icon.png" alt="CodeChat" width="70" style="margin-top: 20px">

<br>Felvin-CodeChat</h1>

<div align="center">
<h2>

Use the power of OpenAI's ChatGPT LLM model to write, refactor, generate, and more!

</h2>

</div>

With just one click, you can create files/projects, fix your code, or utilize OpenAI's official ChatGPT APIs without any configuration! Simply put your API key in the settings, and begin!

# Features

The extension includes a context menu of commands that enables you to send the chosen text or code to the ChatGPT service and display the output in the ChatGPT panel. This panel allows you to copy or move the code to the current file or create a new file and then move the result there.

# API Key

Upon installation, you will be prompted to enter your OpenAI API key.
as an alternative you can also enter it into your Visual Studio Code settings.json file:

```
{
  "codechat.apiKey": "YOUR API KEY"
}
```

# Available Commands

- ChatGPT: Ask Anything
- ChatGPT: Refactor Code
- ChatGPT: Generate Comment
- ChatGPT: Generate Code
- ChatGPT: Generate Tests
- ChatGPT: Find Bugs
- ChatGPT: Optimize Code
- ChatGPT: Explain Code
- ChatGPT: Clear Conversation
- ChatGPT: Export Conversation
- ChatGPT: Rewrite Selection
- ChatGPT: Send Selection

---

### Refactor Code

<img src="./images/refactor-code.png" alt="Refactor Code" width="800"/>

---

### Generate Comment

<img src="./images/generate-comment.png" alt="Generate Comment" width="800"/>

---

### Generate Code

<img src="./images/generate-code.png" alt="Generate Code" width="800"/>

---

### Generate Tests

<img src="./images/generate-test.png" alt="Generate Tests" width="800"/>

---

### Find Bugs

<img src="./images/find-bugs.png" alt="Find Bugs" width="800"/>

---

### Optimize Code

<img src="./images/optimize-code.png" alt="Optimize Code" width="800"/>

---

### Explain Code

<img src="./images/explain-code.png" alt="Explain Code" width="800"/>

---

### Rewrite Selection

<img src="./images/rewrite-selection.png" alt="Rewrite Selection" width="800"/>

---

# Customize your code prompts or use defaults

```json
        "codechat.promptPrefix.addTest": {
          "default": {
            "default": "Generate tests:"
          },
          "description": "The prompt prefix used for adding tests for the selected code",
          "type": "object"
        },
        "codechat.promptPrefix.summarize": {
          "description": "The prompt prefix used for summarizing text.",
          "default": "Summarize text: ",
          "type": "string"
        },
        "codechat.promptPrefix.comment": {
          "default": {
            "default": "Generate short comment: "
          },
          "description": "The prompt prefix used to generate comment for selected code.",
          "type": "object"
        },
        "codechat.promptPrefix.explain": {
          "default": {
            "default": "Explain code: "
          },
          "description": "The prompt prefix used for explaining the selected code",
          "type": "object"
        },
        "codechat.promptPrefix.findProblem": {
          "default": {
            "default": "Find problems: "
          },
          "description": "The prompt prefix used for finding problems for the selected code",
          "type": "object"
        },
        "codechat.promptPrefix.generate": {
          "default": {
            "default": "Generate code: "
          },
          "description": "The prompt prefix used generate code base on text",
          "type": "object"
        },
        "codechat.promptPrefix.optimize": {
          "default": {
            "default": "Optimize code: "
          },
          "description": "The prompt prefix used for optimizing the selected code",
          "type": "object"
        },
        "codechat.promptPrefix.refactor": {
          "default": {
            "default": "Refactor code and explain what's changed: "
          },
          "description": "The prompt prefix used for refactoring the selected code",
           "type": "object"
        },
        "codechat.promptPrefix.rewrite": {
          "default": "Rewrite following sentence: ",
          "description": "Will try to rewrite sentences.",
          "type": "string"
        }
```

If you wish to set prompts based on file type, simply include the file name and the prompt value you desire:

```json
        "codechat.promptPrefix.addTest": {
          "typescript": "Generate tests typescript:"
        }
```

## Set Prompts Base on File type

# Extension Options

```json
        "codechat.apiKey": {
          "description": "Openai api key to communicate with chatgpt api",
        },
        "codechat.maxTokens": {
          "default": 1000,
          "description": "The maximum number of [tokens](/tokenizer) to generate in the completion.  The token count of your prompt plus `max_tokens` cannot exceed the model's context length. Most models have a context length of 2048 tokens (except for the newest models, which support 4096).",
        },
        "codechat.model": {
          "default": "text-davinci-003",
          "description": "ID of the model to use. You can use the [List models](/docs/api-reference/models/list) API to see all of your available models, or see our [Model overview](/docs/models/overview) for descriptions of them.",
        }
```

# Caveats & Limitations

The conversation panel may give the impression of conversing with ChatGPT, but in reality it does not. The extension relies on the official OpenAPI library to interact with the ChatGPT API, and unfortunately, this library currently lacks a conversation API. Therefore, the extension can only provide a response to the immediate question posed, and is unable to recall any previous exchanges.

# Disclaimer

- There are no assurances that this extension will operate seamlessly and without any adverse effects. Therefore, it is recommended that you exercise caution while using it, as it may undergo modifications that are beyond our control. For instance, OpenAI may introduce unanticipated changes to some or all of its functionalities, which could potentially affect the performance of this extension.

- The extension will employ an API Key that is saved in the settings.json file. It is important to note that VS Code has the ability to synchronize this key across its various instances, and this is not within the purview of this extension. If this is a concern for you, it is recommended that you refrain from utilizing the extension.

- The extension will solely gather metadata to enhance its functionalities, and it will not gather any personally identifiable information. You have the option of enabling or disabling telemetry by setting either 'telemetry.telemetryLevel' or 'codechat.telemetry.disable' to their corresponding values. The extension will only collect metadata if both of these settings have permitted telemetry.

- We cannot be held responsible for any problems that may occur as a result of using this extension. It should also be noted that your use of OpenAI services is subject to OpenAI's own terms and conditions.

# Credits
- This extension was inspired by and based on [gencay/vscode-chatgpt](https://github.com/gencay/vscode-chatgpt)
