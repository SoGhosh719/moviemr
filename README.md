# 🎬 Movie Rating Histogram (MapReduce with MRJob)

This project uses the [MRJob](https://mrjob.readthedocs.io/en/latest/) library to compute a histogram of movie ratings using MapReduce in Python. Each movie's ID is mapped to the number of times it has been rated.

---

## 📁 Input Format

The input dataset should be a tab-separated file (`.tsv`) with the following structure per line:

userID movieID rating timestamp

shell
Copy
Edit

### 🔸 Example:
1 10 4.0 964982703 2 10 5.0 964981247 3 20 3.0 964982224

yaml
Copy
Edit

---

## ⚙️ How It Works

This script runs in two MapReduce steps:

### 1. Mapper
- Extracts `movieID` from each line.
- Emits `(movieID, 1)` to represent one rating.

### 2. Reducer
- Aggregates the counts for each `movieID`.
- Outputs total number of ratings per movie.

---

## 🧪 Output Example

Given the above sample input, the output would be:
"10" 2 "20" 1

yaml
Copy
Edit

---

## ▶️ How to Run

Make sure you have `mrjob` installed:

```bash
pip install mrjob
Then run the job using:

bash
Copy
Edit
python rating_histogram.py < input.txt
Or if you want to run it on Hadoop:

bash
Copy
Edit
python rating_histogram.py -r hadoop < input.txt
🧰 Requirements
Python 3.x

mrjob library

Install using:

bash
Copy
Edit
pip install mrjob
