# Google Play Store Review Reply Bot

This repository contains a Python script that fetches the latest reviews (from the last week) from a specified Google
Play Store app and replies to them using OpenAI's GPT-3.5-turbo.

## Requirements

- Python 3.x
- Google API Python Client
- OpenAI Python
- PyYAML

## Installation

1. Clone this repository.

2. Install the required Python packages:

```sh
pip install -r requirements.txt
```

3. Configure the `config.yaml` file with your settings:

    - `app_package_name`: The package name of your Android app.
    - `key_file`: The path to the JSON file containing your Google API service account key.
    - `openai_key`: Your OpenAI API key.
    - `dry_run`: Set to `True` if you want to test the script without actually replying to the reviews.
    - `pre_prompt`: The pre-prompt text that will be sent to GPT-3.5-turbo before the user's review.

4. Run the script:

```sh
   python main.py
```

## Limitations

1. The Google Play Developer API only returns reviews submitted within the last week.

## Usage with a Service Account

To access the Google Play Developer API, a service account must be used. Make sure to configure the `key_file` setting in the `config.yaml` file with the path to your service account JSON key file.

You can create a service account for the Playstore API by going to the Setup > API Access menu of the playstore console