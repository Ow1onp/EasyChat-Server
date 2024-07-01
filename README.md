---

<p align="center">
    <img src="path_to_your_logo_image">
</p>

<h1 align="center">EasyChat Q&A System</h1>

<div align="center">

EasyChat is designed to manage and serve question-answer pairs with ease using FastAPI, SQLAlchemy, and various other Python libraries. It supports functionalities such as CRUD operations on Q&A pairs, photo management, license verification, and fuzzy matching for question-answer retrieval. Additionally, it integrates with the RWKV server for model-based Q&A and logs statistics for user interactions.

[![license][license-image]][license-url]
[![py-version][py-version-image]][py-version-url]

[English](README.md)

</div>

## Features

- **Database Operations**: Manage Q&A pairs with CRUD operations.
- **Q&A Management**: Add, delete, clear, and retrieve Q&A pairs with fuzzy matching for better question-answer retrieval.
- **License Verification**: Ensure authorized use with cryptographic methods and time tampering detection.
- **API Endpoints**: FastAPI endpoints for managing Q&A pairs, photos, and settings.
- **RWKV Server Management**: Manage the lifecycle of the RWKV server process for model-based Q&A.
- **Statistics Logging**: Track interactions, errors, and unlogged questions.
- **Character Counting**: Utility functions for counting and filtering Chinese characters, English letters, and numbers in text.

## Installation

### Prerequisites

- Python 3.7+
- FastAPI
- SQLAlchemy
- jieba
- fuzzywuzzy
- pandas
- openpyxl
- requests
- uvicorn
- aiohttp
- PIL (Pillow)

### Steps

1. Directly double-click to open `server.exe` to run the server and open the webpage at [http://127.0.0.1:9098/](http://127.0.0.1:9098/).
2. Click the register button, copy the machine code, and provide it to the administrator to receive a license key.
3. Enter the license key on the webpage [http://127.0.0.1:9098/](http://127.0.0.1:9098/) to start using the system normally.

## Usage

### API Endpoints

- **Add Q&A Pair**: `POST /add_qa/`
- **Get Q&A Data**: `GET /qa_data/`
- **Update Q&A Pair**: `PUT /update_qa/{id}`
- **Delete Q&A Pair**: `DELETE /delete_qa/{id}`
- **Clear All Q&A Pairs**: `POST /clear_qa/`
- **Upload Photos**: `POST /upload_photos/`
- **Clear All Photos**: `DELETE /clear_photos/`
- **Verify License**: `POST /verify_license`
- **Get UUID**: `GET /get_uuid`
- **Reset License**: `POST /reset_license`
- **Upload File**: `POST /upload_file/`
- **Export Q&A Pairs**: `GET /export_qa_pairs/`
- **Start RWKV Server**: `POST /start_rwkv_server`
- **Stop RWKV Server**: `POST /stop_rwkv_server`
- **Get Settings**: `GET /settings`
- **Modify Settings**: `POST /settings_modify`
- **Get Stats**: `GET /stats`
- **Get Unlogged Questions**: `GET /unlogged_questions`
- **Clear Unlogged Questions**: `POST /clear_unlogged_questions`

## Directory Structure

- **database.py**: Database operations and photo management.
- **easychat.py**: Q&A management and fuzzy matching.
- **licenseauth.py**: License verification and time tampering detection.
- **server.py**: FastAPI server setup and endpoints.
- **startrwkv.py**: RWKV server management.
- **stats_manager.py**: Statistics logging.
- **word_count.py**: Character counting utilities.

## License

This project is licensed under the terms of the MIT license. See `LICENSE` for more details.

## Contact

For any inquiries or issues, please contact the project maintainers at [contact@example.com](mailto:contact@example.com).

---

[license-image]: http://img.shields.io/badge/license-MIT-blue.svg
[license-url]: ./LICENSE
[py-version-image]: https://img.shields.io/pypi/pyversions/fastapi.svg
[py-version-url]: https://pypi.org/project/fastapi/

---
