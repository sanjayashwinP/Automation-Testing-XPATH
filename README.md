# Automation-Testing-XPATH
### Code
```

from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import Select
import time

driver = webdriver.Chrome()
driver.maximize_window()

driver.get("https://www.selenium.dev/selenium/web/web-form.html")

print("TC01 - Registration page opened")

driver.find_element(
    By.XPATH,
    "//input[@name='my-text']"
).send_keys("Sanjay")

print("TC02 - Student name entered")

driver.find_element(
    By.XPATH,
    "//input[@name='my-password']"
).send_keys("Sanjay@123")

print("TC03 - Password entered")

submit_button = driver.find_element(
    By.XPATH,
    "//button[text()='Submit']"
)

print("TC04 - Submit button located")

driver.find_element(
    By.XPATH,
    "//input[contains(@name,'text')]"
)

print("TC05 - Textbox located using contains()")

driver.find_element(
    By.XPATH,
    "//input[starts-with(@name,'my-')]"
)

print("TC06 - Element located using starts-with()")

driver.find_element(
    By.XPATH,
    "//input[@type='text' and @name='my-text']"
)

print("TC07 - Element located using AND")

driver.find_element(
    By.XPATH,
    "//input[@type='password' or @name='my-text']"
)

print("TC08 - Element located using OR")

driver.find_element(
    By.XPATH,
    "//input[@name='my-text']/parent::*"
)

print("TC09 - Parent element found")

driver.find_element(
    By.XPATH,
    "//input[@name='my-text']/ancestor::form"
)

print("TC10 - Ancestor form found")

driver.find_elements(
    By.XPATH,
    "//form/child::input"
)

print("TC11 - Child inputs found")

driver.find_element(
    By.XPATH,
    "//input[@name='my-text']/following::*[1]"
)

print("TC12 - Following element found")

checkbox = driver.find_element(
    By.XPATH,
    "//input[@type='checkbox' and @name='my-check']"
)

if not checkbox.is_selected():
    checkbox.click()

print("TC13 - Checkbox selected")

radio = driver.find_element(
    By.XPATH,
    "//input[@type='radio' and @name='my-radio']"
)

if not radio.is_selected():
    radio.click()

print("TC14 - Radio button selected")

dropdown = driver.find_element(
    By.XPATH,
    "//select[@name='my-select']"
)

Select(dropdown).select_by_visible_text("Two")

print("TC15 - Dropdown selected")

driver.find_element(
    By.XPATH,
    "(//input)[2]"
)

print("TC16 - Second input located")

submit_button.click()

time.sleep(2)

print("TC17 - Form submitted")

all_inputs = driver.find_elements(
    By.XPATH,
    "//input"
)

print("TC18 - Total input fields:", len(all_inputs))

driver.find_element(
    By.XPATH,
    "//input[contains(@name,'my-')]"
)

print("TC19 - Dynamic element found")

print("TC20 - Complete registration automation completed")

input("Press Enter to close the browser...")

driver.quit()

```

### Output
<img width="1903" height="935" alt="image" src="https://github.com/user-attachments/assets/4f7c13d8-75b9-4ae0-8b3a-fdf7dde48981" />
<img width="1913" height="978" alt="image" src="https://github.com/user-attachments/assets/12cc901a-41c1-46ab-8ad2-1e21331e0422" />


