# tutorials
Tutorial for Developments

## Setup for Sphinx

1. Create a virtual environment
```bash
python3 -m venv venv
```

2. Activate the virtual environment
```bash
source venv/bin/activate
```

3. Install required dependencies
```bash
pip install -r requirements.txt
```
4. Build the documentation
```bash
make html
```

5. Open the documentation
```bash
open _build/html/index.html
```