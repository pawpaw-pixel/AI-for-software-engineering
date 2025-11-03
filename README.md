# AI-for-software-engineering
week 4 assignment

TASK ONE:

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

#200 WORD ANALYSIS

The AI-generated function is more concise, readable, and efficient. It uses Python’s built-in sorted() function, which implements Timsort, an algorithm optimized for real-world data with an average and worst-case time complexity of O(n log n). The use of a lambda expression makes the sorting process clear and Pythonic.

In contrast, the manual implementation uses a bubble sort algorithm with nested loops, leading to a time complexity of O(n²). While it demonstrates the logic behind sorting, it is inefficient for large datasets and more error-prone to write or modify.

AI-powered tools like GitHub Copilot and Tabnine leverage pattern recognition from large codebases to produce optimized and idiomatic solutions instantly. This saves time, reduces human error, and promotes best coding practices. However, human understanding is still essential to verify correctness, handle edge cases, and maintain control over algorithmic efficiency.

Conclusion:

✅ AI version — more efficient, maintainable, and elegant.
❌ Manual version — slower but good for learning fundamentals.

TASK TWO:

# AI-Generated Selenium Python Test for Login Page

from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys
import time

driver = webdriver.Chrome()
driver.get("https://www.saucedemo.com/login")

# ✅ Test 1: Valid Credentials

driver.find_element(By.ID, "username").send_keys("validUser")
driver.find_element(By.ID, "password").send_keys("validPass")
driver.find_element(By.ID, "loginButton").click()
time.sleep(2)
assert "Dashboard" in driver.title
print("✅ Valid login test passed")

# ❌ Test 2: Invalid Credentials

driver.get("https://www.saucedemo.com/login")
driver.find_element(By.ID, "username").send_keys("wrongUser")
driver.find_element(By.ID, "password").send_keys("wrongPass")
driver.find_element(By.ID, "loginButton").click()
time.sleep(2)
assert "Invalid" in driver.page_source
print("✅ Invalid login test passed")

driver.quit()


🧾 150-Word Summary

AI-driven testing tools like Selenium IDE with AI plugins and Testim.io enhance the automation process by learning from user interactions and adapting to UI changes automatically. Traditional scripts often fail when elements like buttons or input fields change identifiers, but AI-powered tools use visual recognition and self-healing locators to maintain test reliability. This dramatically improves test coverage and reduces maintenance effort.

In this login test, AI ensures both valid and invalid credential scenarios are tested efficiently with minimal manual updates. The tool can even suggest additional edge cases, such as empty fields or locked accounts, improving overall quality assurance. Compared to manual testing, AI-driven automation provides faster feedback loops, higher accuracy, and continuous adaptability across UI versions — saving time and ensuring more stable software releases.
✅ AI version — more efficient, maintainable, and elegant.
❌ Manual version — slower but good for learning fundamentals.
