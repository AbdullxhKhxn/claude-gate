# Claude Gate: High-Performance OAuth Proxy for Claude API

![Claude Gate](https://img.shields.io/badge/Claude%20Gate-v1.0.0-brightgreen.svg) ![Go](https://img.shields.io/badge/Language-Go-blue.svg) ![License](https://img.shields.io/badge/License-MIT-yellow.svg)

## Overview

Claude Gate is a Go-based OAuth proxy designed specifically for Anthropic's Claude API. It allows Pro and Max subscribers to access the API without incurring additional costs. This project is a rewrite of the claude-auth-bridge, focusing on enhancing performance, security, and ease of distribution. By presenting itself as "Claude Code," it leverages the official CLI for seamless integration.

## Features

- ✅ **OAuth PKCE Authentication**: Utilizes a secure authentication flow to ensure safe access for Claude Pro and Max users.
  
- ✅ **System Prompt Injection**: Automatically identifies as Claude Code, providing a smooth user experience.

- ✅ **Model Alias Mapping**: Handles `latest` model aliases efficiently, ensuring you always use the most current models.

- ✅ **SSE Streaming Support**: Fully supports streaming responses, allowing for real-time data processing.

- ✅ **Cross-Platform Compatibility**: Runs on both macOS and Linux, making it accessible for a wide range of users.

- ✅ **Interactive Dashboard**: Offers real-time monitoring of requests and usage statistics, enhancing usability.

- ✅ **High Performance**: Maintains low memory usage (<50MB) and minimal request overhead (<5ms), ensuring quick responses.

## Quick Start

### 1. Install

**Option A: Build from Source**

To build Claude Gate from source, ensure you have Go installed on your machine. Follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/AbdullxhKhxn/claude-gate.git
   cd claude-gate
   ```

2. Build the application:
   ```bash
   go build -o claude-gate
   ```

3. Run the application:
   ```bash
   ./claude-gate
   ```

**Option B: Download Pre-built Binary**

Visit the [Releases](https://github.com/AbdullxhKhxn/claude-gate/releases) section to download the latest version. Choose the appropriate binary for your operating system and execute it directly.

### 2. Configuration

Before using Claude Gate, configure it with your API keys. Create a configuration file named `config.yaml` in the root directory:

```yaml
oauth:
  client_id: YOUR_CLIENT_ID
  client_secret: YOUR_CLIENT_SECRET
  redirect_uri: YOUR_REDIRECT_URI
```

Replace `YOUR_CLIENT_ID`, `YOUR_CLIENT_SECRET`, and `YOUR_REDIRECT_URI` with your actual credentials.

### 3. Running the Proxy

To start the proxy, run the following command:

```bash
./claude-gate -config config.yaml
```

This will start the server, and you can begin making requests to the Claude API.

## Usage

Once the server is running, you can access the API through the proxy. Use your preferred HTTP client to send requests. Here's an example using `curl`:

```bash
curl -X POST http://localhost:8080/api/your-endpoint \
-H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
-d '{"key":"value"}'
```

Make sure to replace `YOUR_ACCESS_TOKEN` with the token you receive after authentication.

## Interactive Dashboard

Claude Gate features an interactive dashboard for monitoring your API usage. Access it by navigating to `http://localhost:8080/dashboard` in your web browser. The dashboard provides insights into:

- Total requests made
- Successful responses
- Error rates
- Real-time usage statistics

## Troubleshooting

If you encounter issues while using Claude Gate, consider the following steps:

1. **Check Logs**: Review the application logs for any error messages.
2. **Configuration**: Ensure your `config.yaml` file is correctly set up.
3. **Network Issues**: Verify your network connection and ensure that the API is accessible.
4. **Documentation**: Refer to the official documentation for additional guidance.

## Contributing

Contributions are welcome! If you'd like to contribute to Claude Gate, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push your branch to your fork.
5. Submit a pull request.

## License

Claude Gate is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Links

For more information, visit the [Releases](https://github.com/AbdullxhKhxn/claude-gate/releases) section. Download the latest version and get started with Claude Gate today!

## Contact

For questions or feedback, please open an issue in the repository or reach out via the GitHub Discussions section.

---

![Claude API](https://example.com/claude-api-image.png)

---

Explore the capabilities of Claude Gate and enhance your experience with the Claude API. With its robust features and user-friendly interface, you can maximize your productivity and streamline your workflows.