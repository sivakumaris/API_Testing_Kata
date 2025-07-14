# 🧪 Booking API – Automation Framework

This project is a robust API automation framework using **Java**, **TestNG**, and **RestAssured**, enriched with **Allure Reporting** for dynamic, insightful test visualization. It’s designed for easy onboarding, modular scalability, and professional-grade reporting.

It covers:
- CRUD operations via APIs
- Validation of Create Booking API and Delete Booking API
- Create booking API fields validation and error responses
- Logging and reporting with Allure
- CI-ready Maven setup

---

## 📦 Technologies Used

- Java 11+
- Maven 3.6+
- TestNG
- RestAssured
- Allure Report
- IntelliJ IDEA

---

## 🚀 Getting Started

### 🔧 Requirements
Before you run the project, make sure you have the following installed:

#### Install in IntelliJ
- Java 17 SDK
- Maven (Bundled or install separately)
- IntelliJ Plugins:
  - **TestNG** (Settings > Plugins > Marketplace)
  - **Allure Test Report** (optional, for preview inside IDE)


#### Install Allure CLI (Required for generating reports)
🟢 **For Windows:**
choco install allure
    
🟢 **For Mac (Homebrew):**
brew install allure

🟢 **For Linux:**
sudo apt install allure
After installing, **run allure --version** to verify

---

## Project Setup in IntelliJ

1. Clone the project:
   git clone https://github.com/sivakumaris/API_Testing_Kata.git
2. Open the project in IntelliJ IDEA.
3. Set SDK:
   File → Project Structure → Project SDK → Java 11+
4. Enable annotation processing:
   - File → Settings → Build, Execution, Deployment → Compiler → Annotation Processors
   - Check "Enable annotation processing"
5. Install IntelliJ Plugins (recommended):
    - TestNG
    - Allure Framework

---

## 🧪 Running the Tests
### ▶️ Run via IntelliJ (testng.xml)
1. Locate testng.xml in the root directory.
2. Right-click → Run testng.xml.

### 🔁 Run via Maven
1. mvn clean test
   Or specify the suite file
2. mvn clean test -DsuiteXmlFile=testng.xml

---

##  📊 Generating Allure Report
After test execution, Allure results are saved to allure-results

### ✅ Generate and View Report
- allure generate allure-results --clean -o allure-report
- allure open allure-report

---

## 🌐 Hosting the Report on GitHub Pages
1. Switch to gh-pages branch or create one:
    - git checkout --orphan gh-pages
    - git rm -rf .
    - cp -r allure-report/* .
    - git add .
    - git commit -m "Deploy Allure report"
    - git push origin gh-pages
      
2. Go to your repo → Settings → Pages
    - Source: gh-pages
    - Folder: /root
    - Your report will be live at your Repo.Similar like:
      https://sivakumaris.github.io/API_Testing_Kata/

---

## ⚠️ Troubleshooting
### ❗ Tests not running?
  1. Check if testng.xml includes your test classes
  2. Confirm IntelliJ is using Java 17
  3. Try: Build > Rebuild Project in IntelliJ

### ❗ Allure not recognized?
  1. Check if Allure CLI is in system PATH
  2. Restart terminal or system after installation













