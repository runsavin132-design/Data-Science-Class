# 📊 Data Science-Python Environment Setup Guide
### **Course: Data Science & Statistical Analysis with Python**
**Instructor:** RUN Savin

## 1. Download & Install Anaconda
Anaconda is our "Main Factory." It manages our Python versions and all the professional libraries we will use in this course.

1.  **Download:** Go to [anaconda.com/download](https://www.anaconda.com/download) and download the Windows installer.
2.  **Install:** Run the `.exe` file. 
    * Click **Next** and **I Agree**.
    * Select **"Just Me"**.
    * **Note:** Keep the default installation path and settings.
3.  **Finish:** Once the green bar is full, click **Finish**. Uncheck the boxes for "Launch Navigator" and "Welcome" to keep things fast.

---

## 2. Install Visual Studio Code (VS Code)
VS Code is the professional editor where we will write our scripts and notebooks.

1.  **Download:** Go to [code.visualstudio.com](https://code.visualstudio.com/).
2.  **Install:** Run the installer. 
    * **Important:** Check the box that says **"Add to PATH"**.
    * Check **"Create a desktop icon"** for easy access.

---

## 3. Create & Setup the Environment
We use a specific "virtual environment" to ensure everyone has the same Python version (3.10) and libraries.

### A. Create the Environment
1.  Open the **Anaconda Prompt** (search for it in your Windows Start Menu).
2.  Paste this command and press **Enter**:
    ```bash
    conda create --name ds_course python=3.10 -y
    ```

### B. Install Data Science Libraries
1.  In the same window, **activate** the new room:
    ```bash
    conda activate ds_course
    ```
2.  Now, install our toolkit in one go:
    ```bash
    conda install pandas numpy matplotlib seaborn statsmodels ipykernel -y
    ```
    *(If the download stops due to internet issues, simply press the **Up Arrow** and **Enter** to resume.)*

---

## 4. Connect VS Code to the Environment
This step tells VS Code to use the `ds_course` tools we just installed.

1.  Open **VS Code**.
2.  Go to the **Extensions** icon (left sidebar squares) and install the **"Python"** extension by Microsoft.
3.  Press **`Ctrl + Shift + P`** on your keyboard to open the Command Palette.
4.  Type **"Python: Select Interpreter"** and click it.
5.  Select: **`Python 3.10.x ('ds_course': conda)`**.

---

## 5. Final Success Test
To verify everything is correct, create a new file named `check_setup.py` and run this code:

```python
import pandas as pd
import seaborn as sns
import statsmodels.api as sm
import sys

print("--- Environment Check ---")
print(f"✅ Python Version: {sys.version.split()[0]}")
print(f"✅ Pandas Version: {pd.__version__}")
print(f"✅ Seaborn Version: {sns.__version__}")
print("-------------------------")
print("🚀 Your Data Science workstation is fully ready!")
