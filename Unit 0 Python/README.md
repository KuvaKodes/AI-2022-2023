# Unit 0 Python

Warm-up Python exercises: basic scripting (`Python_Excercises.py`, `Python_Excercises_2.py`), Project Euler problems (`ProjectEuler.py`), and a heap/set performance exercise (`Data_Structures.py`).

## About the `*file1.txt` / `*file2.txt` / `*file3.txt` inputs

`Data_Structures.py` takes three file paths as command-line arguments
(`python3 "2 Vardhan Kushaan Data_Structures.py" f1 f2 f3`) and reads them as
lists of newline-separated integers to exercise `set`/`dict`/`heapq`
operations at different input sizes. Each size tier (`10k`, `100k`, `1m`,
`10m`) is just N lines of generated integers — not meaningful data.

The `10mfile1.txt`, `10mfile2.txt`, `1mfile1.txt`, and `1mfile2.txt` variants
(~75 MB and ~6.6 MB each) were removed from version control to keep the repo
lean. The smaller `10k`/`100k` tiers and the `*file3.txt` companions were left
in place since they're small enough to be harmless.

To regenerate a removed file for a size of N lines, e.g.:

```python
with open("10mfile1.txt", "w") as f:
    for i in range(10_000_000):
        f.write(f"{i}\n")
```

(Use whatever value/range matches the exercise you're rerunning — the original
generation logic wasn't preserved beyond "N lines of integers".)
