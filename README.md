# AlphaSentra
Australia — ASX 300 — Data collection — processing.

## Database connection
In MongoDB Atlas: Make sure the IP Access list includes where the script is running from.
For testing — Access all IP address: 0.0.0.0/0

## Install Packages
To run this script, you need to make sure of the requirements:

`pip install -r requirements.txt`


## Usage

Run the application interactively:
```bash
python main.py
```

Or run in batch processing mode directly:
```bash
python main.py -batch
```

Reset all datasets:
```bash
python main.py -reset
```

Enforce database size limit (optional MB value):
```bash
python main.py -dblimit [MB]
```

The `-batch` flag executes `run_batch_processing()` without showing the menu interface.
The `-reset` flag executes `reset_all()` to reset document statuses and clean up one-time records.
The `-dblimit` flag executes `enforce_db_size_limit()` to manage database storage quotas.