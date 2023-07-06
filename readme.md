# CV Automation Script

This script is designed to automate various tasks related to CV processing, including proofreading, scraping job postings, and generating new CVs. It utilizes the GPT-3.5 Turbo model from OpenAI to perform these tasks.

## Prerequisites

Before running the script, ensure that you have the following:

- Python installed on your system
- Required Python packages: `json`, `html2text`, `click`, `openai`, `requests`

## Installation

1. Clone the repository or download the script file.

2. Install the required Python packages by running the following command:

   ```
   pip install -r requirements.txt
   ```

## Usage

Run the script using the following command:

```
python cvgpt.py [options]
```

### Options

- `--cv_file`, `-cv`: Specify the path to the CV file for proofreading or generating a new CV.
- `--url`, `-u`: Provide the URL of the job posting to scrape.
- `--action`, `-a`: Choose the action to perform. Valid values are: `proofread`, `scrape`, `generate`.

### Actions

1. **Proofread**: Proofreads the provided CV file and saves the output as a new file. To use this action, provide the `--cv_file` option with the path to the CV file and set the `--action` option to `proofread`.

   Example:

   ```
   python cvgpt.py --cv_file path/to/cv.txt --action proofread
   ```

2. **Scrape**: Scrapes the job posting from the provided URL and saves it as a new file. To use this action, provide the `--url` option with the URL of the job posting and set the `--action` option to `scrape`.

   Example:

   ```
   python cvgpt.py --url https://example.com/job-posting --action scrape
   ```

3. **Generate**: Generates a new CV based on the provided CV file and the job posting. Additionally, a cover letter is generated. To use this action, provide the `--cv_file` option with the path to the CV file and set the `--action` option to `generate`. This action requires a job posting to be scraped first.

   Example:

   ```
   python cvgpt.py --cv_file path/to/cv.txt --action generate
   ```

**Note**: The CV file must be in plain text format. The generated CV and cover letter will be saved as Markdown files.

## Configuration

The script reads configuration settings from a `config.json` file. Make sure to provide the required information in the config file before running the script. The configuration file should include the following:

```json
{
  "openai_api_key": "YOUR_OPENAI_API_KEY"
}
```

## License

This script is licensed under the [MIT License](LICENSE). Feel free to modify and distribute it as needed.