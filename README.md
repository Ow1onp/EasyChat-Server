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

1. Clone the repository:
   ```sh
   git clone <repository_url>
   cd easychat
   ```

2. Install the required dependencies:
   ```sh
   pip install -r requirements.txt
   ```

3. Set up the database:
   ```sh
   python -m database
   ```

4. Create necessary directories:
   ```sh
   mkdir -p data/photo data/uploads
   ```

## Usage

### Running the Server

To start the FastAPI server, run:
```sh
python server.py
```

### API Endpoints

#### Q&A Management

- **Add Q&A Pair**
  ```sh
  POST /add_qa/
  ```

- **Get Q&A Data**
  ```sh
  GET /qa_data/
  ```

- **Update Q&A Pair**
  ```sh
  PUT /update_qa/{id}
  ```

- **Delete Q&A Pair**
  ```sh
  DELETE /delete_qa/{id}
  ```

- **Clear All Q&A Pairs**
  ```sh
  POST /clear_qa/
  ```

#### Photo Management

- **Upload Photos**
  ```sh
  POST /upload_photos/
  ```

- **Clear All Photos**
  ```sh
  DELETE /clear_photos/
  ```

#### License Management

- **Verify License**
  ```sh
  POST /verify_license
  ```

- **Get UUID**
  ```sh
  GET /get_uuid
  ```

- **Reset License**
  ```sh
  POST /reset_license
  ```

#### Export/Import Data

- **Upload File**
  ```sh
  POST /upload_file/
  ```

- **Export Q&A Pairs**
  ```sh
  GET /export_qa_pairs/
  ```

#### RWKV Server Management

- **Start RWKV Server**
  ```sh
  POST /start_rwkv_server
  ```

- **Stop RWKV Server**
  ```sh
  POST /stop_rwkv_server
  ```

#### Settings Management

- **Get Settings**
  ```sh
  GET /settings
  ```

- **Modify Settings**
  ```sh
  POST /settings_modify
  ```

#### Statistics Management

- **Get Stats**
  ```sh
  GET /stats
  ```

- **Get Unlogged Questions**
  ```sh
  GET /unlogged_questions
  ```

- **Clear Unlogged Questions**
  ```sh
  POST /clear_unlogged_questions
  ```

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

## Contributing

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add new feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a Pull Request.

## Contact

For any inquiries or issues, please contact the project maintainers at [contact@example.com](mailto:contact@example.com).

---

[license-image]: http://img.shields.io/badge/license-MIT-blue.svg
[license-url]: ./LICENSE
[release-image]: https://img.shields.io/github/release/your_username/your_repository.svg
[release-url]: https://github.com/your_username/your_repository/releases/latest
[py-version-image]: https://img.shields.io/pypi/pyversions/fastapi.svg
[py-version-url]: https://pypi.org/project/fastapi/

---

Replace `path_to_your_logo_image` with the actual path to your logo image, and update the `repository_url` with your actual repository URL. Adjust any other placeholders with your specific information as needed.
