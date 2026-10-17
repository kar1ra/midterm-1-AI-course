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

Chosen candidate: B, k=5

(Decision, using your intervals and the budget. Give the recall of your choice for EN, RU and KK separately.)
I started with $18000. Both options A stand 20573 and 27474 $, so I threw them off. From B I chose k=5: it costs 15352 $, recall 0.850 (0.739–0.919). B, k=3 recall 0.617 (0.490–0.729). Intervals do not intersect, so I consider k=5 to prove better. Recall B, k=5 languages: EN 0.95, RU 0.75, KK 0.85. Worst of all is served by RU, and this 43 % of traffic. Questions on 20 on language, intervals wide, so the en–RU gap I do not consider proved. A, k=5 (0.628–0.842) intersects with B, k=5, so the advantages A I don't see, and it is out of budget.

### 1e. Next measurement (at most 60 words)
I would add at least 100 new questions to the language, especially in Russian, and re-measured B, k=5. If recall RU remains about 0.75 at a narrow interval, Ru lag is proven and I would pick up the size of chanca or k for RU within the budget.

## Part 2: A document pipeline you can defend

### 2a. Numbers

| pipeline | overall accuracy | weakest cell (language, condition) | accuracy there | lower | upper | annual cost |
|---|---|---|---|---|---|---|
| H | 0.894| KK, degraded| 0.833| 0.664| 0.927| 8821|
| L | 0.811| KK, degraded| 0.733| 0.556| 0.858| 9000|

Personal-data pages per year sent abroad under H:

### 2b. Memo (at most 300 words)

Operations manager.
Someone is served worse. I found that both pipline weaker than anything on the Kazakh with a complex Sky. H: 25/30 = 0.833 (0.664–0.927). L: 22/30 = 0.733 (0.556–0.858), the same L on KK clean. Intervals intersect, so the difference H and L I don't think proven. Total accuracy (H 0.894, L 0.811) conceals this weakness. In the cell only 30 documents, so that confidence is low
Personal data (three questions of lecture 5.1). When H scanner goes to the TSOD abroad. Who keeps it and how long, I don't know, it's necessary to find out at wendor in writing. His application does not replace the check for compliance with law No. 94-V. under H abroad 20400 pages with iin per year. When L scan remains on the bank server in Kazakhstan, stores the bank, we specify the term ourselves. Find out who has access to the server
Audited measures. I would introduce: a contract with the vendor on the storage and training on data (if H); mask name and iin before sending; access log to the scans; 30 days removal period with monthly check; manual check of KK degred sample
My choice: L. it costs $ 9000 against $ 8821, the difference is small. The accuracy of L is lower, but in a weak cell difference is not proven, and data remain in the country. Residual risk: low accuracy at Kazakh (0.733). I would reduce it by hand checking and test on more Kazakh scans

## Part 3: Explain your own numbers

### Q1

Number:2.14
Why (at most 40 words):
I noticed that the conclusion is 5 times more expensive input. KK input grew 2.49 times, output only 1.44, so the share of expensive withdrawal in the account fell, and the account grew smaller (2.14) than tokens (2,39)

### Q2

Number:44.4%
Why (at most 40 words):
I counted: English is cut (920 e5-tokens at a limit of 512), RU (448) and KK (266) are placed. The cut tail does not fall into embedding, and the search will not find information from it

### Q3

Number:67.4%
Why (at most 40 words):
I left Monday, Friday, Sunday (95.9 %) and moved. Top-p cuts the tail, and the temperature changes the shape of the distribution and does not remove anything

### Q4

Number:30
Why (at most 40 words):
I came to the fact that the leaderboard prefers X (67 against 63) because errors are not fined. The model learns to guess, not to say "I don't know", hence hallucinations. At a fine ahead Y

### Q5

Number:15.9
Why (at most 40 words):
 I received 318 tokens on the parameter against 20 Chinchilla, i.e. the model is re-obuchen on this criterion. Chinchilla claimed that GPT-3 and similar models are not available: there are many parameters, data is little
 
