# Merge Time Ranges (Node.js Module)

## 📘 Description
This Node.js module merges overlapping or nearly-continuous time ranges based on a configurable threshold.  
It ensures the output is sorted, non-overlapping, and easy to use for analytics or time-series data cleaning tasks.

---

## 🧠 Function Signature
```js
/**
 * Merges discontinuous time ranges within a given threshold.
 * @param {Array<[number, number]>} ranges - Array of [start, end) ranges (unsorted, may overlap)
 * @param {number} threshold - Max gap (in ms) allowed between ranges to still be merged
 * @returns {Array<[number, number]>} - Sorted, non-overlapping merged ranges
 */
```
---

## ⚙️ Installation
Clone this repository and install dependencies (if any):
```bash
git clone https://github.com/YOUR_USERNAME/merge-time-ranges.git
cd merge-time-ranges
npm install
```

---

## 🚀 Example Usage
```js
const { mergeTimeRanges } = require('./mergeTimeRanges');

const ranges = [
  [1000, 2000],
  [2500, 4000],
  [3900, 4100],
  [8000, 9000],
  [9050, 9500]
];
const threshold = 200;

console.log(mergeTimeRanges(ranges, threshold));
// Output: [ [1000, 2000], [2500, 4100], [8000, 9500] ]
```

---

## 🧪 Test
To run example tests:
```bash
node test.js
```

---

## 🧩 Example Inputs & Outputs

### Example 1
**Input:**
```js
ranges = [
  [1000, 2000],
  [2500, 4000],
  [3900, 4100],
  [8000, 9000],
  [9050, 9500]
]
threshold = 200
```
**Output:**
```js
[ [1000, 2000], [2500, 4100], [8000, 9500] ]
```

### Example 2
**Input:**
```js
ranges = [
  [0, 10],
  [15, 20],
  [25, 30]
]
threshold = 4
```
**Output:**
```js
[ [0, 10], [15, 20], [25, 30] ]
```

### Example 3
**Input:**
```js
ranges = [
  [0, 10],
  [12, 15],
  [17, 25],
  [27, 35]
]
threshold = 3
```
**Output:**
```js
[ [0, 35] ]
```

---

## 🧑‍💻 Author
**Yogendra Dayal**  
B.Tech CSE, Ajay Kumar Garg Engineering College (2026 Batch)  
📧 yogendradayal3@gmail.com  
🔗 [GitHub](https://github.com/yogendra) | [LinkedIn](https://linkedin.com/in/yogendra)

---

## 🪪 License
This project is licensed under the [ISC License](https://opensource.org/licenses/ISC).
