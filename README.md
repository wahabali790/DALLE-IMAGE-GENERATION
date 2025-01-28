# DALLE Image Generator

This project demonstrates how to generate an image using OpenAI's DALL-E model through Python.

## Features

- Generates an image based on a given text prompt.
- Uses DALL-E 3 model to produce high-quality images.
- Output includes a URL for the generated image.

## Requirements

Make sure you have the following installed:

- Python 3.7 or higher
- OpenAI Python library

## Installation

1. Install the OpenAI Python package:

   ```bash
   pip install openai
   ```

## Configuration

1. Obtain your OpenAI API key from [OpenAI](https://platform.openai.com/).

2. Set up your API key in the script:

   ```python
   from openai import OpenAI
   client = OpenAI()
   ```

## Usage

1. Run the script to generate an image:

   ```python
   from openai import OpenAI

   client = OpenAI()

   response = client.images.generate(
       model="dall-e-3",
       prompt="whale fish",
       size="1024x1024",
       quality="standard",
       n=1,
   )

   print(response.data[0].url)
   ```

2. The script will output a URL for the generated image. You can open the URL in your browser to view the image.

## How It Works

- **Model:** The script uses the DALL-E 3 model to generate images based on a given text prompt.
- **Prompt:** The text prompt `"whale fish"` is provided to generate an image.
- **Output:** The generated image is returned as a URL.

## Example Output

For the prompt `"whale fish"`, the script might generate a URL like:

```
https://openai.com/some_generated_image_url
```

You can copy and paste the URL into your browser to view the generated image.

## License

This project is licensed under the MIT License. Feel free to use and modify it as needed.

## Acknowledgements

- [OpenAI](https://openai.com/) for the DALL-E model.
