# Auto-Translate CLI

The **Auto-Translate CLI** is a command-line tool for translating text files using the Auto-Translate API. It allows users to specify the source language, target language, input file, and output file to automate the translation process directly from the command line.

## Prerequisites

- **Node.js** (v12+)
- **Auto-Translate API Key**: Obtain an API key from [auto-translate.com](https://auto-translate.com) and set it as an environment variable.
- **API Key Environment Variable**: Set the `AUTO_TRANSLATE_API_KEY` environment variable to your API key:
  ```bash
  export AUTO_TRANSLATE_API_KEY="your-api-key"
  ```

## Usage

The CLI accepts multiple options for customizing the translation:

```bash
npx @auto-translate/cli -sf <sourceFile> -tf <targetFile> -sl <sourceLanguage> -tl <targetLanguage>
```

### Options

| Option                   | Description                                                    |
| ------------------------ | -------------------------------------------------------------- |
| `-sf, --source-file`     | Path to the source JSON file for translation                   |
| `-tf, --target-file`     | Path to save the translated content                            |
| `-sl, --source-language` | Language code of the source text (e.g., `en` for English)      |
| `-tl, --target-language` | Language code for the target language (e.g., `es` for Spanish) |

### Example

To translate a file from English to Spanish, use:

```bash
npx @auto-translate/cli -sf en.json -tf es.json -sl en -tl es
```

### Version

Check the version with:

```bash
@auto-translate/cli -v
```

## Environment Variables

- **AUTO_TRANSLATE_API_KEY**: Set this environment variable to your API key from auto-translate.com.

## Error Handling

The CLI includes error handling for:

1. **Missing Required Options**: If any required options are missing, the CLI will display help instructions and exit.
2. **API Errors**: If there are issues with the API request (e.g., no subscription or invalid request), relevant messages will be displayed.
3. **Not Fully Translated**: If the translation is not fully completed, wait a minute and run the command again to complete the translation.

## License

MIT License

## Acknowledgments

Auto-Translate CLI utilizes the [auto-translate.com](https://auto-translate.com) API to provide seamless translations.
