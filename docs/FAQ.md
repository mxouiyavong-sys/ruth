# Frequently Asked Questions (FAQ)

## General

### What is Ruth?
Ruth is a local-first, token-free AI with a continuous-time mind built completely from scratch in Python and NumPy (with a dependency-free C runtime). She has no pretrained model, no API keys, no internet connection, and no tokenizers.

### How does Ruth work without tokens?
Instead of cutting text into discrete tokens from a static vocabulary, Ruth reads characters and signals continuously (as 9 continuous signal channels akin to voltages), processing them through liquid neural networks, a state-space field, and energy-basin memories.

### Is Ruth private and offline?
Yes. Everything Ruth learns stays locally in a single folder on your computer (`~/.local/share/ruth` or `RUTH_HOME`). She never communicates with external servers or APIs.

---

## Usage

### How do I wake Ruth up?
Run:
```sh
ruth app
```
This opens her local browser interface on `127.0.0.1`. Alternatively, you can use the terminal interface:
```sh
ruth talk
```

### How do I teach Ruth something privately?
Wrap private parts in `{{ }}`, or use the `--private` flag:
```sh
ruth teach --private secret.txt
```
or inside `ruth talk`:
```sh
/private The door code is 1234
```

### How do I run tests and benchmarks?
To run the test suite:
```sh
python -m pytest
```
To benchmark Ruth against online n-gram baselines:
```sh
ruth bench
```

---

## Contributing

### What are the core contribution principles?
1. **Token-free**: No tokenizer or pretrained model.
2. **Self-contained**: Python standard library + numpy only; C runtime must remain dependency-free C99.
3. **Security is her judgment**: Privacy relies on her discretion and training, not external keys or filters.
4. **Measured, not assumed**: Changes must be accompanied by measurements (`ruth bench` or tests).

### How do I submit changes?
Fork the repository, create a feature branch, ensure all tests pass (`python -m pytest`), and submit a pull request following project guidelines.
