# AI-for-software-engineering
week 4 assignment

# AI-Suggested Code
def sort_dicts_by_key(data, key):
    return sorted(data, key=lambda x: x[key])

# Manual Code
def sort_dicts_by_key_manual(data, key):
    n = len(data)
    for i in range(n):
        for j in range(0, n - i - 1):
            if data[j][key] > data[j + 1][key]:
                data[j], data[j + 1] = data[j + 1], data[j]
    return data
records = [
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 20},
    {"name": "Charlie", "age": 23}
]

print(sort_dicts_by_key(records, "age"))
print(sort_dicts_by_key_manual(records, "age"))

The AI-generated function is more concise, readable, and efficient. It uses Python’s built-in sorted() function, which implements Timsort, an algorithm optimized for real-world data with an average and worst-case time complexity of O(n log n). The use of a lambda expression makes the sorting process clear and Pythonic.

#200 WORD ANALYSIS
In contrast, the manual implementation uses a bubble sort algorithm with nested loops, leading to a time complexity of O(n²). While it demonstrates the logic behind sorting, it is inefficient for large datasets and more error-prone to write or modify.

AI-powered tools like GitHub Copilot and Tabnine leverage pattern recognition from large codebases to produce optimized and idiomatic solutions instantly. This saves time, reduces human error, and promotes best coding practices. However, human understanding is still essential to verify correctness, handle edge cases, and maintain control over algorithmic efficiency.

Conclusion:
✅ AI version — more efficient, maintainable, and elegant.
❌ Manual version — slower but good for learning fundamentals.
