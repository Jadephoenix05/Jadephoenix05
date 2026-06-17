# Visual Studio Code Jupyter Notebook Configuration Guide

> [!TIP]
> **Troubleshooting Note:** If you experience unexpected execution errors or the notebook fails to connect, try uninstalling and reinstalling the **Python** and **Jupyter** extensions in VS Code, then restart the application.

This guide outlines the complete setup required to configure and run Jupyter Notebooks natively within Visual Studio Code.

---

## 1. Install Required VS Code Extensions
1. Open **VS Code**.
2. Click the **Extensions icon** on the left sidebar or press `Ctrl+Shift+X` (`Cmd+Shift+X` on macOS).
3. Search for **Python** (by Microsoft) and click **Install**.
4. Search for **Jupyter** (by Microsoft) and click **Install**.

## 2. Set Up Your Python Environment & Dependencies
You must have a Python environment equipped with the `ipykernel` package to execute notebook cells.
1. Open the integrated terminal in VS Code using `Ctrl+`` (backtick).
2. Create and activate a virtual environment (recommended):
   ```bash
   python -m venv .venv
   ```
   * **Windows:** `.venv\Scripts\activate`
   * **macOS/Linux:** `source .venv/bin/activate`
3. Install the required Jupyter packages:
   ```bash
   pip install notebook ipykernel
   ```

## 3. Create or Open a Notebook
* **Option A:** Press `Ctrl+Shift+P` (`Cmd+Shift+P` on macOS) to open the Command Palette, type `Jupyter: Create New Jupyter Notebook`, and press **Enter**.
* **Option B:** Create a new file via the Explorer panel and name it with the **`.ipynb`** extension (e.g., `analysis.ipynb`).

## 4. Select the Kernel
1. Look at the **top right corner** of your opened notebook file.
2. Click on **Select Kernel**.
3. Choose **Python Environments...** and select the path to your active virtual environment or Python installation (look for the one marked "Recommended").

## 5. Verify the Setup
1. Type a quick test line in your first code cell:
   ```python
   print("Jupyter is working!")
   ```
2. Press **`Shift+Enter`** or click the **Play icon** to the left of the cell to execute it. The output will display directly below the cell.
