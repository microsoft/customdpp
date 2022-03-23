# Custom Display-Post-Processor (aka "Custom DPP")

## Overview

Automatic Speech Recognition output display format is critical to downstream tasks and one-size doesn’t fit all. Custom Display-Post-Processor (aka "Custom DPP") allows users to define their own lexical-to-display format rules to improve the speech recognition service quality on top of [Microsoft Azure Custom Speech Service](https://docs.microsoft.com/azure/cognitive-services/speech-service/custom-speech-overview).

![cdpp demo](pics/CDPP.jpg)

## Features and capabilities

### Supported features
* Rewrite the final output of Microsoft ASR
* Add new profanity words to filter out from output
* Edit advanced ITN rules (invert-text-normalization, supports on en-us only)

### Supported locales

:white_check_mark: en-us :white_check_mark: pt-br :white_check_mark: pt-pt :white_check_mark: it-it :white_check_mark: es-es 

:white_check_mark: es-mx :white_check_mark: fr-fr :white_check_mark: fr-ca :white_check_mark: zh-cn :white_check_mark: ja-jp 

### Supported service regions

:white_check_mark: West US :white_check_mark: West US2 :white_check_mark: East US :white_check_mark: East US2 :white_check_mark: Central US

:white_check_mark: Central India :white_check_mark: North Europe :white_check_mark: West Europe :white_check_mark: East Asia :white_check_mark: Japan East :white_check_mark: Southeast Asia

## Get start with Custom DPP CLI

See the [Get Start](GETSTART.md) document about how to download and use the CLI tool to upload, evaluate, and deploy your custom display format models.

See the [Concept](CONCEPTS.md) document about the basic concepts of Microsoft display post processing.

## Supported operations

The general format of Custom DPP CLI commands is: `cdpp [command] [arguments] --[flag-name] [flag-value]`

Available Commands:
* `init` - Create and init a project, scaffolding it with template files
* `push` - Push the custom model files or test set to Microsoft Speech server
* `eval` - Evaluate the latest model pushed to the Microsoft Speech server
* `deploy` - Deploy a custom DPP model and bind to a custom speech model
* `get` - Get model, test set, evaluation or deployment detail information from Microsoft Speech server
* `check` - Check the format/grammar of the custom rule dataset rewrite, profanity and ITN
* `config` - Config subscription key or service region of a project, or get the current project settings
* `delete` - Delete a model, test, eval or deploy from Microsoft Speech server
* `fetch` - Fetch model files or test set from Microsoft Speech server
* `list` - List models, test sets, evaluation or deployment summary information of the subscription from Microsoft Speech server
* `version` - Show version information and supported regions, locales
* `help` - Help about any command

## Find help from your command prompt

For convenience, consider adding the Custom DPP CLI location to your system path for ease of use. That way you can type `cdpp` from any directory on your system.

To see a list of commands, type `cdpp -h` and then press the ENTER key.

To learn about a specific command, just include the name of the command (For example: `cdpp push -h`).

![cdpp command help example](pics/CLI.jpg)

If you choose not to add Custom DPP CLI to your path, you'll have to change directories to the location of your `cdpp` executable and type `cdpp` or `.\cdpp` in Windows PowerShell command prompts.


## Frequently asked questions

### Do we support Bring Your Own Storage?

Not yet. We will add the bring your own storage in public preview.
