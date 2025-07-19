# levenshtein-distance-java
This repository contains four Java-based implementations of the **Levenshtein Distance** algorithm, showcasing its variations and optimizations.

---

## 📌 What is Levenshtein Distance?

Levenshtein Distance is a dynamic programming algorithm that calculates the **minimum number of single-character edits** (insertions, deletions, or substitutions) required to change one string into another.

It is widely used in:
- Spell checkers
- Natural Language Processing (NLP)
- DNA sequence alignment
- Plagiarism detection
- Search engines (fuzzy matching)

---

## 🚀 Project Structure

### 🔹 `Task1.java` – Basic Levenshtein Distance
- Implements the standard edit distance.
- Supports insertion, deletion, and substitution.
- Uses dynamic programming (bottom-up approach).
- Time Complexity: `O(m × n)`
- Space Complexity: `O(m × n)`

### 🔹 `Task2.java` – Custom Cost Levenshtein Distance
- Supports variable operation costs:
  - `Ci` → Cost of insertion
  - `Cd` → Cost of deletion
  - `Cs` → Cost of substitution
- Still uses dynamic programming.
- Useful in cases like spell checkers with cost penalties.

### 🔹 `Task3.java` – Dictionary-based Spell Suggestions
- Suggests corrections for a misspelled word using a dictionary.
- Compares the input word with each word in the dictionary using Task2 logic.
- Finds **all words** with **minimum edit distance** to the input.
- No threshold filtering is used — all minimum-cost words are returned.

### 🔹 `Task4_Optimized.java` – Space-Optimized Levenshtein Distance
- Reduces space complexity from `O(m × n)` to `O(min(m, n))`
- Ideal for large string comparisons.
- Maintains correctness with reduced memory usage.

---

## 🧪 Sample Input / Output

**Input:**
```text
s1: "kitten"
s2: "sitting"
Output:

pgsql
Copy
Edit
Task 1: Minimum Cost = 3
Task 2: Minimum Cost with custom costs (Ci=1, Cd=1, Cs=2) = 4
Task 3: Suggestions for 'cart' = ['card', 'cart']
Task 4: Optimized Minimum Cost = 3
🛠️ Technologies Used
Language: Java

Java Version: Java 8 or above

IDE: IntelliJ IDEA / VSCode / Eclipse (any)

📂 How to Run
Clone the repository:

bash
Copy
Edit
git clone https://github.com/your-username/levenshtein-distance-java.git
cd levenshtein-distance-java
Compile and run each task:

bash
Copy
Edit
javac Task1.java
java Task1
Repeat for Task2.java, Task3.java, Task4_Optimized.java

🧠 Algorithm Summary
Task	Features	Time	Space
Task 1	Basic Edit Distance	O(m×n)	O(m×n)
Task 2	Custom Costs (Ci, Cd, Cs)	O(m×n)	O(m×n)
Task 3	Spell Suggestions from Dictionary	O(k×m×n)	O(m×n) per word
Task 4	Space-Optimized Distance Calculation	O(m×n)	O(min(m, n))

🤝 Contributions
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change or enhance.

📄 License
This project is open-source and free to use under the MIT License.
