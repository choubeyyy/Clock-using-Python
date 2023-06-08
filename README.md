# Clock Project Documentation

This project is a clock developed using Python and Jupyter Notebook. It utilizes the tkinter library to create a graphical user interface (GUI) for displaying the current time.

## Installation

To run this clock project, please make sure you have the following dependencies installed:

- Python (version 3 or above)
- Jupyter Notebook
- tkinter library

## Usage

1. Open the Jupyter Notebook file named "Clock_Project.ipynb" in your Jupyter Notebook editor.

2. Execute the entire code by clicking on "Run" or using the shortcut Shift + Enter.

3. A new window will appear displaying the clock with the current time in a digital format.

4. The clock will continuously update every second to reflect the accurate time.

## Code Explanation

```python
from tkinter import *
from tkinter.ttk import *
from time import strftime

root = Tk()

root.title('Clock')

def time():
    string = strftime('%H:%M:%S %p')
    label.config(text=string)
    label.after(1000, time)
    
label = Label(root, font=("ds-digital", 80), background="black", foreground="cyan")
label.pack(anchor='center')

time()

mainloop()
```

- The code starts by importing the necessary libraries: `tkinter`, `tkinter.ttk`, and `time.strftime`.

- A new window (Tkinter root) is created and titled "Clock".

- The `time()` function is defined, which retrieves the current time using the `strftime()` function from the `time` library. The time is formatted as "%H:%M:%S %p", representing hours, minutes, seconds, and AM/PM.

- The `config()` method is used to update the text of the `label` widget with the current time.

- The `after()` method is called to update the clock every second (1000 milliseconds).

- A `Label` widget is created to display the time. It uses the "ds-digital" font with a font size of 80, a black background, and cyan foreground.

- The `pack()` method is used to position the `label` widget at the center of the window.

- The `time()` function is called initially to display the current time.

- Finally, the `mainloop()` method is called to start the main event loop and keep the window open until the user closes it.

## Contribution

Contributions to this clock project are welcome. If you encounter any issues or have suggestions for improvements, please feel free to submit a pull request or open an issue on the project repository.

## License

This project is licensed under the [MIT License](LICENSE). Feel free to modify and distribute it as per the terms of the license.
