# At work, we had to follow a special procedure to create and close Jira tickets. In this code, I automated this procedure to create a ticket with Python, and when the work is done, close the ticket and lock the system.

# What is Selenium
Selenium Python bindings provides a simple API to write functional/acceptance tests using Selenium WebDriver. Through Selenium Python API you can access all functionalities of Selenium WebDriver in an intuitive way.

Selenium Python bindings provide a convenient API to access Selenium WebDrivers like Firefox, Ie, Chrome, Remote etc. The current supported Python versions are 3.5 and above.

# Python code

import time

from selenium import webdriver
from selenium.webdriver.chrome.service import Service
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
import ctypes

chrome_web_driver = Service("C:\Chrome Driver\chromedriver.exe")
driver = webdriver.Chrome(service=chrome_web_driver)
wait = WebDriverWait(driver, 30)
driver.get(*Link*)
driver.set_window_position(0, 0)
driver.set_window_size(1280, 900)

// user_name
login_form_username = wait.until(EC.element_to_be_clickable((By.ID, 'ID')))
login_form_username.clear()
login_form_username.send_keys(*username*)

// Password
login_form_password = wait.until(EC.element_to_be_clickable((By.ID, 'ID')))
login_form_password.clear()
login_form_password.send_keys(*password*)

// log_in
login_form_submit = wait.until(EC.element_to_be_clickable((By.ID, 'ID')))
login_form_submit.click()

// sleep time
time.sleep(3)

// issues
find_link = wait.until(EC.element_to_be_clickable((By.XPATH, 'XPATH')))
find_link.click()

// My open issues
open_issues = wait.until(EC.element_to_be_clickable((By.XPATH, 'XPATH')))
open_issues.click()

// inprogress
action_id_5 = wait.until(EC.element_to_be_clickable((By.XPATH, 'XPATH')))
action_id_5.click()

// resolution
resolution = wait.until(EC.element_to_be_clickable((By.ID, 'ID')))
resolution.click()

time.sleep(5)

// issues_done
Done = wait.until(EC.element_to_be_clickable((By.XPATH, 'XPATH')))
Done.click()

// issue-workflow-transition-submit
issue_workflow_transition_submit = wait.until(EC.element_to_be_clickable((By.ID, 'ID')))
issue_workflow_transition_submit.click()

// sleep time
time.sleep(5)

// quit
driver.quit()

// sleep time
time.sleep(2)

// lock
ctypes.windll.user32.LockWorkStation()


