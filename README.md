# GroupDNA: Your WhatsApp Group Chat, Decoded[cite: 2]
*Spotify Wrapped, but for your friend group.*[cite: 2]

## Overview
GroupDNA is a behavioral analytics tool that parses raw WhatsApp chat exports to generate a comprehensive, visually structured personality and activity report[cite: 4]. It calculates headline statistics, plots an activity heatmap, extracts top vocabulary, calculates response speeds, and assigns a specific personality archetype (like "The Spammer" or "The Night Owl") to every participant[cite: 3, 14].

<img width="411" height="630" alt="Screenshot 2026-10-02 215801" src="https://github.com/user-attachments/assets/d479e446-4b45-4a83-978e-f0d1224f04a9" />

## The Technical Constraint
This project was built to demonstrate constraint discipline and mastery of core programming concepts[cite: 24]. Anyone can throw libraries at a problem, but this tool was built from scratch without them[cite: 24]. 

**What I Used:**
* Python Fundamentals (variables, loops, conditionals, functions, lists, dicts, sets, tuples, f-strings)[cite: 2, 17].
* `datetime` (specifically `datetime.strptime` and `timedelta` for computing response gaps)[cite: 17].
* `NumPy` (specifically for the 2D matrix powering the activity heatmap)[cite: 17].
* Standard `open()` for File I/O[cite: 17].

**What I Strictly Forbade:**
* ❌ `pandas` (no DataFrames or `read_csv`)[cite: 17].
* ❌ `matplotlib`, `seaborn`, or `plotly` (all visualizations are strictly text-based)[cite: 17].
* ❌ `re` (regex - all pattern matching relies on standard string methods)[cite: 17].
* ❌ `collections.Counter` or `collections.defaultdict`[cite: 17].
* ❌ Any AI/ML libraries (like `scikit-learn` or `nltk`)[cite: 17].

## The 7-Day Build Log
This project was developed incrementally over 7 days[cite: 18]:
* **Day 1:** Built the core parser to read the text file, extract timestamps/senders, and isolate system messages, omitted media, and deleted messages[cite: 18].
* **Day 2:** Computed the group overview, total message counts, and date ranges[cite: 18].
* **Day 3:** Engineered the word-frequency dictionary, defined stop-words, and extracted the top 10 group-wide words[cite: 18].
* **Day 4:** Developed a 6x24 `NumPy` matrix to track per-person, per-hour message counts, rendering it into a visual terminal heatmap[cite: 18].
* **Day 5:** Parsed timestamps into `datetime` objects to compute average response times and track the longest consecutive silent streaks[cite: 18].
* **Day 6:** Designed and implemented the detection logic for 8 unique personality archetypes (plus one custom archetype, "The Philosopher"), ensuring exclusive assignment based on normalized scoring[cite: 19].
* **Day 7:** Polished the final output formatting using f-string alignment and block characters to create a shareable, screenshot-ready report[cite: 19].

## How to Run
1. Clone this repository.
2. Export a WhatsApp group chat (Select "Without Media").
3. Rename the exported `.txt` file to `hostel_bois.txt` (or update the filename directly in the code)[cite: 4, 18].
4. Run `GroupDNA_Gaurav_DS24039.ipynb` in Google Colab or Jupyter Notebook[cite: 25].

---
**Author:** Gaurav Mahesh Bodhe
**Roll Number:** DS24039
