# Internet Speed Tester

This Python script uses the `tkinter` and `speedtest` libraries to create a simple GUI application that tests internet speed (download speed, upload speed, and ping).

## Dependencies

* **tkinter:** Used for creating the graphical user interface.  (Usually comes pre-installed with Python)
* **speedtest-cli:** Used to measure internet speed. You can install it using pip:
    ```bash
    pip install speedtest-cli
    ```

## Functionality

The script provides the following functionalities:

* **Download Speed Test:** Measures the download speed of the internet connection.
* **Upload Speed Test:** Measures the upload speed of the internet connection.
* **Ping Test:** Measures the ping (latency) to servers.
* **GUI Interface:** Presents a user-friendly interface with buttons to initiate each test.
* **Results Display:** Displays the test results in a pop-up message box.
* **Unit Conversion:** Automatically converts the speed to appropriate units (bps, Kbps, Mbps, Gbps).

## Code Explanation

1.  **Import Libraries:**
    ```python
    import tkinter
    from tkinter import *
    import speedtest
    import tkinter.messagebox
    ```
2.  **`downloadSpeed()`, `uploadSpeed()`, `ping()` Functions:**
    * These functions set the `option` variable to indicate which test to perform.
    * They then call the `showSpeed()` function to execute the test.
3.  **`showSpeed()` Function:**
    * Creates a `speedtest.Speedtest()` object.
    * Performs the selected test (`download()`, `upload()`, or `get_servers()` and `results.ping`).
    * Formats the speed with appropriate units.
    * Displays the result using `tkinter.messagebox.showinfo()`.
4.  **GUI Creation:**
    * Creates the main window using `tkinter.Tk()`.
    * Sets the title, size, and background color.
    * Adds labels to instruct the user.
    * Creates buttons for "Check Download Speed", "Check Upload Speed", and "Check Ping", each linked to its respective function.
    * The `wn.mainloop()` loop keeps the window running until it is closed.

## How to Run

1.  **Install Dependencies:** Make sure you have Python installed and then install the `speedtest-cli` library using pip.
2.  **Save the Code:** Save the code as a `.py` file (e.g., `internet_speed_test.py`).
3.  **Execute the Script:** Run the script from the command line:
    ```bash
    python internet_speed_test.py
    ```

The GUI window will appear, and you can click the buttons to perform the speed tests.
