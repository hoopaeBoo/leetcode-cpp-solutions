# 📘 LeetCode C++ Solutions

This repository contains categorized **LeetCode solutions in C++**, structured for easy navigation and reference.  
Each problem is **organized by topic**, making it easier to find and practice specific algorithms.

---

## 📂 Categories
Each category contains problems and their solutions. Click on a section to expand it.

<details>
<summary><strong>Array</strong></summary>

- [1. Two Sum.md](Array/1.%20Two%20Sum.md)

</details>

<details>
<summary><strong>Backtracking</strong></summary>


</details>

<details>
<summary><strong>Biconnected Componen</strong></summary>


</details>

<details>
<summary><strong>Binary Indexed Tree</strong></summary>


</details>

<details>
<summary><strong>Binary Search</strong></summary>


</details>

<details>
<summary><strong>Binary Search Tree</strong></summary>


</details>

<details>
<summary><strong>Binary Tree</strong></summary>


</details>

<details>
<summary><strong>Bit Manipulation</strong></summary>


</details>

<details>
<summary><strong>Bitmask</strong></summary>


</details>

<details>
<summary><strong>Brainteaser</strong></summary>


</details>

<details>
<summary><strong>Breadth-First Search</strong></summary>


</details>

<details>
<summary><strong>Bucket Sort</strong></summary>


</details>

<details>
<summary><strong>Combinatorics</strong></summary>


</details>

<details>
<summary><strong>Concurrency</strong></summary>


</details>

<details>
<summary><strong>Counting</strong></summary>


</details>

<details>
<summary><strong>Counting Sort</strong></summary>


</details>

<details>
<summary><strong>Data Stream</strong></summary>


</details>

<details>
<summary><strong>Database</strong></summary>


</details>

<details>
<summary><strong>Depth-First Search</strong></summary>


</details>

<details>
<summary><strong>Design</strong></summary>


</details>

<details>
<summary><strong>Divide and Conquer</strong></summary>


</details>

<details>
<summary><strong>Doubly-Linked List</strong></summary>


</details>

<details>
<summary><strong>Dynamic Programming</strong></summary>


</details>

<details>
<summary><strong>Enumeration</strong></summary>


</details>

<details>
<summary><strong>Eulerian Circuit</strong></summary>


</details>

<details>
<summary><strong>Game Theory</strong></summary>


</details>

<details>
<summary><strong>Geometry</strong></summary>


</details>

<details>
<summary><strong>Graph</strong></summary>


</details>

<details>
<summary><strong>Greedy</strong></summary>


</details>

<details>
<summary><strong>Hash Function</strong></summary>


</details>

<details>
<summary><strong>Hash Table</strong></summary>

- [1. Two Sum.md](Hash%20Table/1.%20Two%20Sum.md)

</details>

<details>
<summary><strong>Heap Priority Queue</strong></summary>


</details>

<details>
<summary><strong>Interactive</strong></summary>


</details>

<details>
<summary><strong>Iterator</strong></summary>


</details>

<details>
<summary><strong>Line Sweep</strong></summary>


</details>

<details>
<summary><strong>Linked List</strong></summary>


</details>

<details>
<summary><strong>Math</strong></summary>


</details>

<details>
<summary><strong>Matrix</strong></summary>


</details>

<details>
<summary><strong>Memoization</strong></summary>


</details>

<details>
<summary><strong>Merge Sort</strong></summary>


</details>

<details>
<summary><strong>Minimum Spanning Tree</strong></summary>


</details>

<details>
<summary><strong>Monotonic Queue</strong></summary>


</details>

<details>
<summary><strong>Monotonic Stack</strong></summary>


</details>

<details>
<summary><strong>Number Theory</strong></summary>


</details>

<details>
<summary><strong>Ordered Set</strong></summary>


</details>

<details>
<summary><strong>Prefix Sum</strong></summary>


</details>

<details>
<summary><strong>Probability and Statistics</strong></summary>


</details>

<details>
<summary><strong>Queue</strong></summary>


</details>

<details>
<summary><strong>Quickselect</strong></summary>


</details>

<details>
<summary><strong>Radix Sort</strong></summary>


</details>

<details>
<summary><strong>Randomized</strong></summary>


</details>

<details>
<summary><strong>Recursion</strong></summary>


</details>

<details>
<summary><strong>Rejection Sampling</strong></summary>


</details>

<details>
<summary><strong>Reservoir Sampling</strong></summary>


</details>

<details>
<summary><strong>Rolling Hash</strong></summary>


</details>

<details>
<summary><strong>Segment Tree</strong></summary>


</details>

<details>
<summary><strong>Shell</strong></summary>


</details>

<details>
<summary><strong>Shortest Path</strong></summary>


</details>

<details>
<summary><strong>Simulation</strong></summary>


</details>

<details>
<summary><strong>Sliding Window</strong></summary>


</details>

<details>
<summary><strong>Sorting</strong></summary>


</details>

<details>
<summary><strong>Stack</strong></summary>


</details>

<details>
<summary><strong>String</strong></summary>


</details>

<details>
<summary><strong>String Matching</strong></summary>


</details>

<details>
<summary><strong>Strongly Connected Component</strong></summary>


</details>

<details>
<summary><strong>Suffix Array</strong></summary>


</details>

<details>
<summary><strong>Topological Sort</strong></summary>


</details>

<details>
<summary><strong>Tree</strong></summary>


</details>

<details>
<summary><strong>Trie</strong></summary>


</details>

<details>
<summary><strong>Two Pointers</strong></summary>


</details>

<details>
<summary><strong>Union Find</strong></summary>


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
