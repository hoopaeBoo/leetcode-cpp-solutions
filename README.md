# 📘 LeetCode C++ Solutions

This repository contains categorized **LeetCode solutions in C++**, structured for easy navigation and reference.  
Each problem is **organized by topic**, making it easier to find and practice specific algorithms.

---

## 📂 Categories
Each category contains problems and their solutions. Click on a section to expand it.

<details>
<summary><strong>Array</strong></summary>

- [1. Two Sum.md](Array/1.%20Two%20Sum.md)
- [4. Median of Two Sorted Arrays.md](Array/4.%20Median%20of%20Two%20Sorted%20Arrays.md)

</details>

<details>
<summary><strong>Binary Search</strong></summary>

- [4. Median of Two Sorted Arrays.md](Binary%20Search/4.%20Median%20of%20Two%20Sorted%20Arrays.md)

</details>

<details>
<summary><strong>Divide and Conquer</strong></summary>

- [4. Median of Two Sorted Arrays.md](Divide%20and%20Conquer/4.%20Median%20of%20Two%20Sorted%20Arrays.md)

</details>

<details>
<summary><strong>Dynamic Programming</strong></summary>

- [10. Regular Expression Matching.md](Dynamic%20Programming/10.%20Regular%20Expression%20Matching.md)
- [5. Longest Palindromic Substring.md](Dynamic%20Programming/5.%20Longest%20Palindromic%20Substring.md)

</details>

<details>
<summary><strong>Hash Table</strong></summary>

- [1. Two Sum.md](Hash%20Table/1.%20Two%20Sum.md)
- [3. Longest Substring Without Repeating Characters.md](Hash%20Table/3.%20Longest%20Substring%20Without%20Repeating%20Characters.md)

</details>

<details>
<summary><strong>Linked List</strong></summary>

- [2. Add Two Numbers.md](Linked%20List/2.%20Add%20Two%20Numbers.md)

</details>

<details>
<summary><strong>Math</strong></summary>

- [2. Add Two Numbers.md](Math/2.%20Add%20Two%20Numbers.md)
- [7. Reverse Integer.md](Math/7.%20Reverse%20Integer.md)
- [9. Palindrome Number.md](Math/9.%20Palindrome%20Number.md)

</details>

<details>
<summary><strong>Recursion</strong></summary>

- [10. Regular Expression Matching.md](Recursion/10.%20Regular%20Expression%20Matching.md)
- [2. Add Two Numbers.md](Recursion/2.%20Add%20Two%20Numbers.md)

</details>

<details>
<summary><strong>Sliding Window</strong></summary>

- [3. Longest Substring Without Repeating Characters.md](Sliding%20Window/3.%20Longest%20Substring%20Without%20Repeating%20Characters.md)

</details>

<details>
<summary><strong>String</strong></summary>

- [10. Regular Expression Matching.md](String/10.%20Regular%20Expression%20Matching.md)
- [3. Longest Substring Without Repeating Characters.md](String/3.%20Longest%20Substring%20Without%20Repeating%20Characters.md)
- [5. Longest Palindromic Substring.md](String/5.%20Longest%20Palindromic%20Substring.md)
- [6. Zigzag Conversion.md](String/6.%20Zigzag%20Conversion.md)
- [8. String to Integer (atoi).md](String/8.%20String%20to%20Integer%20(atoi).md)

</details>

<details>
<summary><strong>Two Pointers</strong></summary>

- [5. Longest Palindromic Substring.md](Two%20Pointers/5.%20Longest%20Palindromic%20Substring.md)

</details>

---

## 🚀 How to Use

### **💻 Running a Solution**
To **compile and run** LeetCode-style C++ code **locally**, you need to:
1. **Wrap the `Solution` class** inside a `main()` function.
2. **Include necessary headers** (`#include <iostream>, <vector>, <unordered_map>`)
3. **Provide input handling** for the `twoSum()` function.
4. **Compile and run** the program.

---

### **✅ Steps**
1. **Create a file**: `two_sum.cpp`
2. **Add a `main()` function** to call `Solution::twoSum()`.
3. **Compile using `g++`**.
4. **Run the executable**.

---

### **📝 Full Working Code (`two_sum.cpp`)**
```cpp
#include <iostream>
#include <vector>
#include <unordered_map>

using namespace std;

class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        unordered_map<int, int> m;
        for (int i = 0; i < nums.size(); ++i) {
            int complement = target - nums[i];
            if (m.count(complement)) return {m[complement], i};
            m[nums[i]] = i;
        }
        return {};
    }
};

int main() {
    Solution solution;

    // Input handling
    vector<int> nums;
    int target, n;

    cout << "Enter number of elements: ";
    cin >> n;
    
    cout << "Enter elements: ";
    nums.resize(n);
    for (int i = 0; i < n; i++) cin >> nums[i];

    cout << "Enter target: ";
    cin >> target;

    // Run twoSum function
    vector<int> result = solution.twoSum(nums, target);

    // Output result
    if (!result.empty()) {
        cout << "Indices: [" << result[0] << ", " << result[1] << "]" << endl;
    } else {
        cout << "No solution found!" << endl;
    }

    return 0;
}
```

---

### **🔧 Compilation & Execution**
#### **1️⃣ Compile the C++ Code**
```bash
g++ -std=c++17 two_sum.cpp -o two_sum
```

#### **2️⃣ Run the Program**
```bash
./two_sum
```

---

### **🎯 Example Run**
#### **Input**
```
Enter number of elements: 4
Enter elements: 2 7 11 15
Enter target: 9
```
#### **Output**
```
Indices: [0, 1]
```

---

### **📌 Summary**
✅ **Wraps the LeetCode `Solution` class** inside `main()`  
✅ **Handles user input** for array and target  
✅ **Compiles and runs locally** using `g++`  
✅ **Displays output in a readable format**  

🚀 **Now you can test LeetCode C++ solutions locally!** 🚀

---

## 🛠 Automate `README.md` Update
This repository includes a script to **automatically update** `README.md` with new files and folders.

### 📝 Script: `update_readme.sh`
1. **Make the script executable**:
   ```bash
   chmod +x update_readme.sh
   ```
2. **Run the script**:
   ```bash
   ./update_readme.sh
   ```

### ✅ Features
- **Scans directories** for new solutions.
- **Uses collapsible sections** (`<details>`) for categories.
- **Formats relative links** (spaces encoded as `%20` for GitHub compatibility).
- **Automatically updates `README.md`** when new files are added.

---

## 📜 License
This project is licensed under the **MIT License**.  
See the full license [here](LICENSE).

---

## 🤝 Contributing
Want to contribute? Here's how:
- **Add a new solution** in the appropriate category.
- **Run `update_readme.sh`** to refresh `README.md`.
- **Submit a pull request** with your solution.

---

## 🔗 References
- [LeetCode](https://leetcode.com/)
- [GeeksforGeeks](https://www.geeksforgeeks.org/)
- [C++ Documentation](https://en.cppreference.com/w/)

---

**🚀 Happy Coding & Algorithm Solving!**
