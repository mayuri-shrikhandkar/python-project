# python-project
import selenium from selenium import webdriver from selenium.webdriver.common.by
import By from selenium.webdriver.support.ui
import WebDriverWait from expected_conditions as EC
import csv
# Set up
webdriver driver = webdriver.Chrome()
# Sign up and navigate to model Hub
driver.get("https://access-corp.com")
#...(complete sign-up and navigation)
# Create and test first model 
model_name = "GTP 40 Mini"
driver.find_element(By.XPATH,"//button[test()='Add New']").click()
driver.find_element(By.NAME,"model_name").send_keys(model_name)
driver.find_element(By.NAME,"model_provider").select_by_visible_text("OpenAl")
driver.find_element(By.NAME,"model_id").select_by_visible_text("GPT 40 MiNi")
driver.find_element(By.XPATH,"//button[text()='Save']").click()
#...(complete testing and deletion)
# Create and test second model
model_name ="GPT 40"
#...(repeat steps for second model)
# Save responses to CSV with open
('response.csv', 'W', newline='') as csvfile:
writer =csv.writer(csvfile)
writer.writerow(["Model Name", "Response"])
write.writerow(model_name, response)
driver.quit()
#
