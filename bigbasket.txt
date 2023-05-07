import time
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.select import Select

driver=webdriver.Chrome()
driver.get("https://www.bigbasket.com/ps/?q=vegetable.")
driver.maximize_window()
dropdownSort=driver.find_element(By.ID,"sel1")
time.sleep(4)
sel=Select(dropdownSort)
time.sleep(3)
#by index
sel.select_by_index(1)
time.sleep(5)
dropdownSort2=driver.find_element(By.XPATH,"//a[@uib-tooltip='Carrot - Orange (Loose)']/../following-sibling::div/child::div/child::span/child::button")
dropdownSort2.click()
time.sleep(5)
qty=driver.find_element(By.XPATH,"//a[@style='text-decoration: none;']")
qty.click()
time.sleep(5)
 