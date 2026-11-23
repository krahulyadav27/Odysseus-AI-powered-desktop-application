# Odysseus – AI-Powered Desktop Application

<p align="center">
  <strong>A Self-Hosted AI Workspace for Productivity, Research, Automation and Intelligent Assistance</strong>
</p>

<p align="center">
  <img src="assets/branding/logo.png" alt="Odysseus Logo" width="150">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.11%2B-blue" alt="Python">
  <img src="https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20%7C%20macOS-lightgrey" alt="Platforms">
  <img src="https://img.shields.io/badge/AI-Self--Hosted-purple" alt="AI">
  <img src="https://img.shields.io/badge/License-AGPL--3.0-green" alt="License">
</p>

---

## 1. Overview

**Odysseus** is a self-hosted AI workspace designed to bring intelligent assistance, automation, research and productivity tools into one unified application.

It provides an integrated environment for interacting with AI models, performing research, managing documents, organizing tasks and connecting external services.

Unlike cloud-only AI applications, Odysseus can run on your own hardware and supports local and API-based AI model workflows.

The application combines a Python backend, an interactive frontend, integrations and supporting services to provide a flexible AI workspace.

## 2. Key Features

### AI Chat and Agents
- Interact with local and cloud-based AI models.
- Use AI agents to perform tasks.
- Connect tools and external services.
- Support for Model Context Protocol (MCP).
- File and document interaction.
- Memory and skill-based workflows.

### Deep Research
- Perform multi-step web research.
- Read and analyze information from sources.
- Generate research reports.
- Organize research workflows.

### AI Model Management
- Discover and configure AI models.
- Hardware-aware model recommendations.
- Download and manage models.
- Support local model-serving workflows.

### Document Management
- Create and edit documents.
- AI-assisted writing and editing.
- Markdown and HTML support.
- CSV and code editing capabilities.

### Email Management
- Connect email accounts using IMAP and SMTP.
- Organize and categorize messages.
- Generate email summaries.
- Draft email replies.

### Productivity Tools
- Notes and task management.
- Calendar integration.
- Reminders and scheduled tasks.
- Session management.

### Additional Capabilities
- Image gallery and image editing.
- Web search.
- Theme customization.
- File uploads.
- External integrations.
- Authentication and security controls.

## 3. Technology Stack

| Component | Technology |
|---|---|
| Backend | Python |
| Backend Framework | FastAPI |
| Frontend | JavaScript, HTML, CSS |
| Package Management | npm |
| Python Dependencies | pip |
| API Communication | HTTP / REST / SSE |
| Database | SQLite and supporting storage services |
| AI Integration | Local and API-based models |
| Containerization | Docker |
| Model Integration | MCP |
| Version Control | Git and GitHub |

## 4. Project Architecture

The application follows a modular architecture that separates backend services, frontend interfaces, integrations and supporting components.

```text
odysseus-dev/
│
├── app.py
├── launcher.py
├── setup.py
│
├── frontend/
│   └── Frontend application
│
├── core/
│   └── Core application logic
│
├── companion/
│   └── Companion functionality
│
├── services/
│   └── Application services
│
├── routes/
│   └── API endpoints
│
├── integrations/
│   └── External integrations
│
├── mcp_servers/
│   └── MCP server components
│
├── config/
│   └── Application configuration
│
├── data/
│   └── Application data
│
├── static/
│   └── Static resources
│
├── assets/
│   └── Application assets
│
├── docs/
│   └── Documentation
│
├── tests/
│   └── Automated tests
│
├── scripts/
│   └── Utility scripts
│
├── website/
│   └── Website resources
│
├── requirements.txt
├── package.json
├── Dockerfile
├── docker-compose.yml
├── .env.example
└── README.md
```

## 5. System Requirements

Before installing the application, ensure your system meets the following requirements.

| Requirement | Recommended |
|---|---|
| Operating System | Windows 10/11, Linux or macOS |
| Python | 3.11 or newer |
| Git | Latest version |
| Node.js | Compatible with the included package configuration |
| RAM | Depends on selected AI models |
| Storage | Depends on installed models and application data |
| Internet | Required for initial setup and online services |

**Note:** Local AI model execution may require additional RAM, GPU memory and storage depending on the selected model.

## 6. Installation and Setup

### Step 1 – Clone the Repository

```bash
git clone https://github.com/krahulyadav27/Odysseus-AI-powered-desktop-application.git
```

Navigate into the project:

```bash
cd Odysseus-AI-powered-desktop-application
```

### Step 2 – Install Python

Install Python 3.11 or newer.

Verify the installation:

```bash
python --version
```

### Step 3 – Create a Virtual Environment

```bash
python -m venv venv
```

Activate it on Windows:

```powershell
.\venv\Scripts\Activate.ps1
```

### Step 4 – Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 5 – Configure Environment Variables

Create your local environment configuration:

```powershell
Copy-Item .env.example .env
```

Open `.env` and configure the required application settings and service credentials.

Never upload your actual `.env` file or private API keys to GitHub.

### Step 6 – Run Application Setup

```bash
python setup.py
```

Follow the setup prompts and complete the required configuration.

## 7. Running the Application

### Option 1 – Windows Launcher (Recommended)

The project includes a Windows launcher script.

Run PowerShell from the project root:

```powershell
powershell -ExecutionPolicy Bypass -File .\launch-windows.ps1
```

The launcher handles the Windows startup workflow, including environment preparation and application startup.

### Option 2 – Run Manually

Activate your virtual environment and execute:

```bash
python -m uvicorn app:app --host 127.0.0.1 --port 7000
```

Once the server starts, open:

**http://localhost:7000**

The application interface should be accessible through your browser.

### Option 3 – Docker

If Docker is installed and configured:

```bash
docker compose up -d --build
```

Check the service logs:

```bash
docker compose logs -f odysseus
```

Refer to the project's Docker configuration and setup documentation for the appropriate deployment port and service configuration.

## 8. Configuration

Odysseus uses environment variables and application settings to configure its services.

Configuration may include:

- Application host and port.
- Authentication settings.
- AI provider credentials.
- Local model endpoints.
- Database and storage settings.
- Email integration.
- External service connections.

Use `.env.example` as the starting point for local configuration.

Do not commit passwords, tokens, private keys or production credentials.

## 9. Security

Security is an important consideration when running a self-hosted AI workspace.

Recommended practices:

- Keep authentication enabled for network-accessible deployments.
- Never publish API keys or passwords.
- Avoid exposing internal service ports publicly.
- Use secure connections when accessing the application remotely.
- Keep dependencies updated.
- Review third-party integrations before enabling them.

See `SECURITY.md` for additional security information.

## 10. Testing

The project includes an automated test suite.

Run tests using:

```bash
pytest
```

For development dependencies, use:

```bash
pip install -r requirements-dev.txt
```

Run individual test files when debugging:

```bash
pytest tests/
```

## 11. Development and Contribution

Contributions and improvements are welcome.

Suggested development workflow:

1. Fork the repository.
2. Create a new branch.
3. Implement your changes.
4. Test the application.
5. Commit your changes.
6. Submit a pull request.

See `CONTRIBUTING.md` for contribution guidelines.

## 12. Future Improvements

Potential areas for further development and customization include:

- Improving the desktop application experience.
- Enhancing Windows installation and startup.
- Improving frontend responsiveness.
- Expanding AI model integrations.
- Enhancing performance and resource management.
- Improving automated testing and deployment.

See `ROADMAP.md` for the project's roadmap.

## 13. License and Attribution

This repository contains source code originating from the upstream Odysseus project.

Original project:

https://github.com/odysseus-dev/odysseus

The upstream project is licensed under **GNU Affero General Public License v3.0 or later (AGPL-3.0-or-later)**.

Original copyright notices, license terms and third-party attribution must be preserved.

See:
- `LICENSE`
- `ACKNOWLEDGMENTS.md`
- `THIRD_PARTY_PROVENANCE.json`

Any modifications and redistribution must comply with the applicable license.

## 14. Repository

**GitHub Repository:**

https://github.com/krahulyadav27/Odysseus-AI-powered-desktop-application

---

<p align="center">
  <strong>Odysseus – Bringing AI, Automation and Productivity Together.</strong>
</p>