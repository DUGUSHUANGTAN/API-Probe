<div align="center">

# API Probe

### A lightweight, single-file API testing tool.

Test API connectivity, explore available models, verify model capabilities, and inspect streaming responses — all from your browser.

**No installation. No backend. Just one HTML file.**

[Features](#-features) · [Getting Started](#-getting-started) · [Supported APIs](#-supported-apis) · [License](#-license)

</div>

---

## ✨ Features

### 🔌 API Connectivity Testing

Quickly verify whether an API endpoint is working correctly.

- Test API connectivity with real requests
- Inspect HTTP status codes and response details
- View request and response information
- Identify common API errors
- Support multiple API protocols

### 🤖 Model Discovery & Verification

Explore models exposed by your API provider.

- Retrieve available model IDs
- Search and filter models
- Inspect model metadata
- Select multiple models for batch verification
- Verify actual model availability through inference requests
- Configure batch concurrency
- Monitor progress and stop ongoing checks

Model discovery and model availability are treated separately.

A model appearing in the API's model list does not necessarily mean it can be successfully invoked.

### 🧠 Model Capability Detection

Verify supported model capabilities through real API requests.

Supported capability tests:

- Text Generation
- Vision
- Tool Calling
- JSON Mode
- Streaming

Capability testing is optional and must be triggered manually.

When available, model metadata is also displayed without requiring additional inference requests.

### ⚡ Streaming & Performance

Inspect streaming responses in real time.

- Real-time streaming output
- Server-Sent Events (SSE) parsing
- Time to First Token (TTFT) measurement
- First response data timing
- Streaming interruption detection
- Request latency measurement

Performance metrics are derived from existing requests whenever possible.

API Probe does not send additional requests solely for benchmarking.

### 🎨 Customizable Interface

A modern interface combining Neo-Brutalism with subtle glass effects.

- Light Mode
- Dark Mode
- Follow System
- English / Chinese
- Persistent appearance preferences
- Responsive layout
- Custom confirmation dialogs

### 🕘 Local History

Keep track of previous API tests.

- View previous test results
- Inspect historical request information
- Delete individual records
- Store history locally in your browser

No external database is required.

---

## 🚀 Getting Started

### Option 1: Download and Run

1. Download the latest HTML file.
2. Open it in a modern browser.
3. Enter your API endpoint and API key.
4. Select the appropriate API protocol.
5. Choose a model and start testing.

That's it.

No installation or local server is required.

### Option 2: Clone the Repository

```bash
git clone https://github.com/DUGUSHUANGTAN/API-Probe.git
```

Open the HTML file in your browser.

> Note: The repository URL assumes the project is published as `API-Probe`.

---

## 🔗 Supported APIs

API Probe supports three API request formats:

| Protocol | Endpoint |
|----------|----------|
| OpenAI Chat Completions | `/v1/chat/completions` |
| OpenAI Responses | `/v1/responses` |
| Anthropic Messages | `/v1/messages` |

Compatible third-party providers and API aggregators may also work.

Actual compatibility depends on the provider's API implementation.

Some providers may support only a subset of the available features.

---

## 🛠️ How It Works

API Probe sends requests directly from your browser to the configured API endpoint.

```text
┌─────────────────────┐
│      API Probe      │
│     Browser UI      │
└──────────┬──────────┘
           │
           │ HTTPS Request
           ▼
┌─────────────────────┐
│    API Provider     │
│                     │
│  OpenAI / Anthropic │
│  Compatible APIs    │
└──────────┬──────────┘
           │
           │ API Response
           ▼
┌─────────────────────┐
│    API Probe        │
│                     │
│ Results & Analysis  │
└─────────────────────┘
```

There is no dedicated API Probe backend.

### Important Notes

**CORS Restrictions**

Because requests are sent directly from the browser, some API providers may block them through Cross-Origin Resource Sharing (CORS) restrictions.

A CORS error does not necessarily indicate that the API itself is unavailable.

**Token Consumption**

Connectivity tests, streaming tests, batch model verification, and capability detection may generate billable API usage.

API Probe displays confirmation prompts for optional detection operations.

**API Key Security**

API keys are sent to the endpoint configured by the user.

Only use trusted API providers.

Avoid entering sensitive credentials into untrusted or modified copies of the application.

---

## 📊 Model Verification Status

| Status | Meaning |
|--------|---------|
| 🟢 Available | The model responded successfully |
| 🔴 Failed | The actual invocation failed |
| 🟡 Inconclusive | The result could not be determined reliably |
| ⚪ Untested | No verification request has been performed |

Model metadata and actual capability verification are displayed separately.

---

## 🌍 Language Support

API Probe currently supports:

- English
- 简体中文

Language and theme preferences are saved locally in the browser.

---

## 📦 Technology

API Probe is built with:

- HTML
- CSS
- Vanilla JavaScript
- Fetch API
- Server-Sent Events (SSE)
- LocalStorage

No frontend framework or build process is required.

---

## ⚠️ Disclaimer

API Probe is an independent API testing utility.

It is not affiliated with OpenAI, Anthropic, or any third-party API provider.

API availability, response behavior, and compatibility depend on the configured provider.

Users are responsible for their own API usage and any associated costs.

---

## 🤝 Contributing

Contributions are welcome!

You can contribute by:

- Reporting bugs
- Suggesting improvements
- Submitting pull requests
- Improving API compatibility
- Enhancing the user interface

Please open an issue before proposing major architectural changes.

---

## 📄 License

This project is licensed under the MIT License.

See the [LICENSE](LICENSE) file for details.

---

<div align="center">

Made by [DUGUSHUANGTAN](https://github.com/DUGUSHUANGTAN)

**Simple. Local. Powerful.**

</div>
