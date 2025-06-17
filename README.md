# Cyeroni SDK Template

A production-ready Python SDK template for building robust API clients with FastAPI integration. This template provides a solid foundation for creating maintainable, well-tested, and fully-typed Python SDKs.

[![Python](https://img.shields.io/badge/python-3.8%20%7C%203.9%20%7C%203.10%20%7C%203.11-blue)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![Imports: isort](https://img.shields.io/badge/%20imports-isort-%231674b1?style=flat&labelColor=ef8336)](https://pycqa.github.io/isort/)

## ✨ Features

- 🚀 **Async-First**: Built with `asyncio` for high-performance API interactions
- 🧠 **Type Annotations**: Full Python type hints for better developer experience
- 🛡️ **Robust Error Handling**: Comprehensive error hierarchy and handling
- 📦 **Structured Project Layout**: Clean separation of concerns
- ✅ **Testing Ready**: Pytest fixtures and examples included
- 📝 **Documentation**: Auto-generated API docs with Sphinx support
- 🔄 **CI/CD Ready**: GitHub Actions workflow included
- 🔒 **Security**: Environment-based configuration and secrets management

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- [Poetry](https://python-poetry.org/) for dependency management
- [Pre-commit](https://pre-commit.com/) hooks (optional but recommended)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/techwithty/cyeroni-sdk-template.git
   cd cyeroni-sdk-template
   ```

2. **Set up the development environment**
   ```bash
   # Install dependencies
   poetry install
   
   # Activate the virtual environment
   poetry shell
   
   # Install pre-commit hooks
   pre-commit install
   ```

3. **Configure environment variables**
   Copy the example environment file and update with your configuration:
   ```bash
   cp .env.example .env
   # Edit .env with your settings
   ```

## 🏗️ Project Structure

```
cyeroni_sdk/
├── .github/                    # GitHub Actions workflows
│   └── workflows/              # CI/CD pipelines
├── _docs/                      # Documentation files
│   ├── examples/               # Usage examples
│   └── api/                    # API reference
├── _tests/                     # Test suite
│   ├── conftest.py             # Pytest configuration
│   ├── test_*.py               # Test modules
│   └── fixtures/               # Test fixtures
├── api/                        # API client implementation
│   ├── models/                 # Data models
│   │   ├── __init__.py
│   │   ├── requests.py         # Request models
│   │   └── responses.py        # Response models
│   ├── route/                  # API route handlers
│   │   ├── __init__.py
│   │   └── ...                 # Route modules
│   └── schemas/                # Pydantic schemas
│       ├── __init__.py
│       └── ...                 # Schema definitions
├── .env.example                # Example environment variables
├── .gitignore                  # Git ignore rules
├── client.py                   # Main client class
├── config.py                   # Configuration handling
├── pyproject.toml              # Project metadata and dependencies
├── pytest.ini                  # Pytest configuration
└── setup.py                    # Package installation script
```

## 🛠️ Usage

### Basic Example

```python
from cyeroni_sdk_template import Client, ClientConfig
import asyncio

async def main():
    # Initialize with default config (loads from environment)
    client = Client()
    
    # Or configure manually
    # config = ClientConfig(
    #     api_key="your-api-key",
    #     base_url="https://api.example.com/v1"
    # )
    # client = Client(config=config)
    
    try:
        # Example API call
        response = await client.example_endpoint.get_example(example_id="123")
        print(f"Response: {response}")
        
    except Exception as e:
        print(f"Error: {e}")

if __name__ == "__main__":
    asyncio.run(main())
```

## 📚 Documentation

For detailed documentation, including API reference and usage examples, see the [documentation](_docs/README.md).

## 🧪 Testing

Run the test suite:

```bash
# Run all tests
pytest

# Run with coverage report
pytest --cov=cyeroni_sdk_template --cov-report=term-missing

# Run a specific test
pytest _tests/test_client.py -v
```

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📧 Contact

TechWithTy - [@techwithty](https://github.com/techwithty)

Project Link: [https://github.com/techwithty/cyeroni-sdk-template](https://github.com/techwithty/cyeroni-sdk-template)

## 🔗 Related Projects

- [FastAPI](https://fastapi.tiangolo.com/)
- [Pydantic](https://pydantic-docs.helpmanual.io/)
- [HTTPX](https://www.python-httpx.org/)

## 📈 Stats

![GitHub last commit](https://img.shields.io/github/last-commit/techwithty/cyeroni-sdk-template)
![GitHub issues](https://img.shields.io/github/issues/techwithty/cyeroni-sdk-template)
![GitHub pull requests](https://img.shields.io/github/issues-pr/techwithty/cyeroni-sdk-template)
