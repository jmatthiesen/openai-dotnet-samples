# OpenAI .NET Samples

Collection of OpenAI samples written in .NET. Similar to the [OpenAI website samples](https://platform.openai.com/examples).

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=623607062&machine=basicLinux32gb&devcontainer_path=.devcontainer.json&location=EastUs)

[![Open in Remote - Containers](https://img.shields.io/static/v1?style=for-the-badge&label=Remote%20-%20Containers&message=Open&color=blue&logo=visualstudiocode)](https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/azure-samples/azure-search-openai-demo)

## Prerequisites

- [Azure Account](https://aka.ms/free)
- Access to [Azure OpenAI](https://learn.microsoft.com/azure/cognitive-services/openai/how-to/create-resource?pivots=web-portal) or [OpenAI](https://openai.com/)
- [VS Code](https://code.visualstudio.com/Download)
- [Polyglot Noteboks VS Code Extension](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.dotnet-interactive-vscode)

## Running samples

**NOTE: The Azure OpenAI Service .NET SDK is currently in preview**

1. Open repository in VS Code. To minimize setup, it's highly recommended you use [Codespaces](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=623607062&machine=basicLinux32gb&devcontainer_path=.devcontainer.json&location=EastUs)
1. Configure environment variables.
    1. Azure OpenAI Service - For more details on how to get these variables, see the [Azure OpenAI documentation](https://learn.microsoft.com/azure/cognitive-services/openai/quickstart?tabs=command-line&pivots=programming-language-csharp#retrieve-key-and-endpoint).
        1. `AOAI_ENDPOINT` - The endpoint for your Azure OpenAI Service.
        1. `AOAI_KEY` - The access key for your Azure OpenAI Service
        1. `AOAI_DEPLOYMENTID` - The name of your model deployment (`davinci-003-deployment`).
    1. OpenAI
        1. `AOAI_DEPLOYMENTID` - The model name (i.e. `text-davinci-003`). For more details on models, see [OpenAI model](https://platform.openai.com/docs/models/gpt-3-5) documentation.
1. Choose a notebook and run it.

## Service notes

The following are things to be mindful of when using each of these model providers. For more information on each of the services, see the [comparing Azure OpenAI and OpenAI](https://learn.microsoft.com/azure/cognitive-services/openai/overview#comparing-azure-openai-and-openai) documentation.

### Azure OpenAI Service

#### Deployment ID

Deployments are a way to provide a user-friendly name for OpenAI models. 

For more details, see the [deploy a model](https://learn.microsoft.com/azure/cognitive-services/openai/how-to/create-resource?pivots=web-portal#deploy-a-model) documentation.

### OpenAI

#### Initialize client

When initializing a client

#### Model Name

Unlike Azure OpenAI Service, OpenAI doesn't use deployments. Instead, it uses the model names. All samples 

## Settings

| Setting | Description |
| --- | --- |
| Model | The name of the OpenAI model. For more details, see the [Azure OpenAI models](https://learn.microsoft.com/azure/cognitive-services/openai/concepts/models) documentation  |
| Max tokens | The maximum number of tokens to generate. The max tokens number can't exceed the number of tokens supported by the model. See the [Azure OpenAI models](https://learn.microsoft.com/azure/cognitive-services/openai/concepts/models#model-summary-table-and-region-availability) documentation for more details on token limits |
| Temperature | A value between 0 and 1 that lets you control how confident the model is when making predictions. Lower temperatures mean less randomness in completion output. |
| Top p | 1 | A value between 0 and 1 that lets you control which tokens to consider in the results. For example a value of 0.1 means only the top 10% are considered. |
| Frequency penalty | A value between -2 and 2. Positive values penalize the text returned based on the frequency of a token frequency. This makes it so there's a lower likelihood of tokens repeating themselves. |
| Presence penalty | A value between -2 and 2. Positive numbers increase the model's likelihood the text returned talks about new topics. |
| Stop Sequence | String values that indicate when the model should stop generating new text. Returned text won't contain the stop sequence. |

## Examples

### Classification

- [Classification](./classification.ipynb)
- [Extract keywords](./extract-keywords.ipynb)
- [Tweet classifier](./tweet-classifier.ipynb)
- [Advanced tweet classifier](./advanced-tweet-classifier.ipynb)

### Generation

- [Parse unstructured data](./parse-unstructured-data.ipynb)
- [Table creator](./table-creator.ipynb)
- [TL;DR summarization](./tldr-summarization.ipynb)
- [Airport code extractor](./airport-code-extractor.ipynb)
- [Extract contact information](./extract-contact-information.ipynb)
- [Notes to summary](./notes-to-summary.ipynb)
- [Grammar correction](./grammar-correction.ipynb)
- [Summarize for 2nd grader](./summarize-second-grader.ipynb)
- [Text to command](./text-to-command.ipynb)
- [Ad from product description](./ad-product-description.ipynb)
- [Product name generator](./product-name-generator.ipynb)
- [Science finction book list maker](./science-fiction-book-list-maker.ipynb)
- [Micro horror story creator](./micro-horror-story-creator.ipynb)
- [Essay outline](./essay-outline.ipynb)
- [VR fitness idea generator](./vr-fitness-idea-generator.ipynb)
- [Recipe creator](./recipe-creator.ipynb)
- [Turn by turn directions](./turn-by-turn-directions.ipynb)
- [Restaurant review creator](./restaurant-review-creator.ipynb)
- [Create study notes](./create-study-notes.ipynb)
- [Create interview questions](./create-interview-questions.ipynb)


### Translation

- [Translate programming languages](./translate-programming-languages.ipynb)
- [Translate English to other languages](./translate-english-other-languages.ipynb)
- [Movie to Emoji](./movie-to-emoji.ipynb)
- [Mood to color](./mood-to-color.ipynb)

### Code

- [C# Bug Fixer](./csharp-bug-fixer.ipynb)
- [C# to Natural Language](./csharp-to-natural-language.ipynb)
- [C# XML Comments](./csharp-xml-comments.ipynb) 
- [Calculate Time Complexity](./calculate-time-complexity.ipynb)
- [JavaScript helper chatbot](./javascript-helper-chatbot.ipynb)
- [SQL translate](./sql-translate.ipynb)
- [SQL request](./sql-request.ipynb)

### Chat

- [Q&A](./qna.ipynb)
- [Factual Answering](./factual-answering.ipynb)
- [Friend Chat](./friend-chat.ipynb)
- [ML/AI language model tutor](./ml-ai-language-model-tutor.ipynb)
- [Marv Sarcastic Bot](./marv-sarcastic-bot.ipynb)
- [Open ended chat](./open-ended-chat.ipynb)

## Additional Resources

- [What is Azure OpenAI Service?](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/overview)
- [Azure SDK for .NET Samples](https://github.com/Azure/azure-sdk-for-net/tree/main/sdk/openai/Azure.AI.OpenAI/tests/Samples)
