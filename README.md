# Facial Recognition Quiz Auth

**Facial Recognition Quiz Auth** is a Python-based authentication system that uses face recognition to verify student identity before allowing access to a quiz exam. It also logs attendance with timestamps in a CSV file.

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install the required libraries.

```bash
pip install face_recognition opencv-python numpy
```

You may also need to install `dlib` (used by `face_recognition`) and `cmake`:

```bash
pip install dlib cmake
```

> Make sure you have a working webcam connected and Python 3.6+ installed.

## Usage

1. Place student face images in the `pics/` directory with filenames matching their names (e.g., `lavanya.jpg`).
2. Modify the list of known student names and image paths in `main.py`.
3. Run the script:

```bash
python main.py
```

### What it does:

- Opens your webcam to detect faces in real-time.
- Compares detected faces with known images.
- If a match is found:
  - Logs the student's name and time in a CSV file named with the current date (e.g., `2025-04-30.csv`).
  - Opens the `success.html` file to allow quiz access.
- If no match:
  - Writes `no access` to `abc.html`.

### Example

```python
# Recognizes Lavanya, logs attendance, opens success.html
# CSV Output: lavanya, 10-34-12
```

## File Structure

```
facial_recognition_quiz/
├── pics/
│   ├── lavanya.jpg
│   ├── csir.jpg
│   └── shrada.jpg
├── success.html
├── Quiz_home.html
├── abc.html
├── main.py
└── 2025-04-30.csv (auto-generated)
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss improvements like:

- Anti-spoofing detection
- Web-based dashboard
- Integration with student databases

Please ensure proper testing and documentation for any changes.

## License

[MIT](LICENSE)
