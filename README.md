# Text Summarization API

A Node.js web service that provides text summarization capabilities using the Hugging Face BART-large-CNN model.

## Description

This project implements a REST API that accepts text input and returns a summarized version using Facebook's BART-large-CNN model through the Hugging Face Inference API. The service is built with Express.js and provides a simple endpoint for text summarization.

## Prerequisites

- Node.js (v12 or higher)
- npm (Node Package Manager)
- Hugging Face API Access Token

## Installation

1. Clone the repository:

```bash
git clone <repository-url>
```

2. Install dependencies:

```bash
npm install
```

3. Create a `.env` file in the root directory and add your Hugging Face API token:

```bash
ACCESS_TOKEN=<your-hugging-face-api-token>
```

## Usage

1. Start the server:

```bash
npm start
```

node public/index.js
```bash
node public/index.js
```


2. The server will start running at `http://localhost:3000`

3. To summarize text, send a POST request to `/summarize` endpoint:

```bash
curl -X POST http://localhost:3000/summarize -H "Content-Type: application/json" -d '{"text_to_summarize": "Your text here"}'
```

     http://localhost:3000/summarize


## API Endpoints

### POST /summarize
Accepts JSON payload with the following structure:

```json
{
  "text_to_summarize": "The text you want to summarize"
}
```

Returns the summarized text as a string.

## Configuration

The summarization parameters can be adjusted in `summarize.js`:
- `max_length`: Maximum length of the summary (default: 100)
- `min_length`: Minimum length of the summary (default: 30)

## Dependencies

- express: Web framework for Node.js
- axios: HTTP client for making API requests

## Error Handling

The API includes basic error handling for:
- API request failures
- Invalid input
- Server errors

## License

[Add your chosen license here]

## Contributing

[Add contribution guidelines if applicable]

## Authors

[Add author information]

## Acknowledgments

- Hugging Face for providing the BART-large-CNN model
- Facebook AI for developing the BART model

