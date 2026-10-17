# Midterm 1: answers

GitHub username: kar1ra
Session code: MAPLE-66
Fingerprint: bdefb948

> Fill in the three lines above from `my_data/DATA.md`. Do not rename headings or table columns: a script reads the numbers.
> Write only in the empty cells and lines. Percentages as 0.78 or 78 %, money as plain numbers.

## AI-use declaration

(About half a page: which assistants or tools you used and for what. If you used none, say so.)

## Part 1: Retrieval and cost decision

### 1a. Metrics (all 60 questions)

| config | recall@1 | recall@3 | recall@5 | MRR@10 |
|---|---|---|---|---|
| A | 0.467|0.683 |0.750 | 0.577|
| B | 0.433| 0.617| 0.850| 0.563|

### 1b. Recall and 95 % Wilson interval of each candidate (recall at its own k)

| candidate | recall@k | lower | upper |
|---|---|---|---|
| A, k=3 | 0.683| 0.558| 0.787|
| A, k=5 | 0.750| 0.628| 0.842|
| B, k=3 | 0.617| 0.490| 0.729|
| B, k=5 | 0.850| 0.739| 0.919|

### 1c. Annual model cost in USD

| candidate | annual cost |
|---|---|
| A, k=3 | 20573|
| A, k=5 | 27474|
| B, k=3 | 13300|
| B, k=5 | 15352|

### 1d. Decision (at most 150 words)

Chosen candidate:

(Decision, using your intervals and the budget. Give the recall of your choice for EN, RU and KK separately.)

### 1e. Next measurement (at most 60 words)

## Part 2: A document pipeline you can defend

### 2a. Numbers

| pipeline | overall accuracy | weakest cell (language, condition) | accuracy there | lower | upper | annual cost |
|---|---|---|---|---|---|---|
| H | 0.894(161/180)| KK, degraded| 0.833(25/30)| 0.664| 0.927| 8821|
| L | 0.811(146/180)| KK, degraded (равна KK, clean)| 0.733(22/30)| 0.556| 0.858| 9000|

Personal-data pages per year sent abroad under H:

### 2b. Memo (at most 300 words)

## Part 3: Explain your own numbers

### Q1

Number:
Why (at most 40 words):

### Q2

Number:
Why (at most 40 words):

### Q3

Number:
Why (at most 40 words):

### Q4

Number:
Why (at most 40 words):

### Q5

Number:
Why (at most 40 words):
