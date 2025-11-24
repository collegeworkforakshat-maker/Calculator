import tkinter as tk
from tkinter import ttk

class CalculatorApp(tk.Tk):
    def __init__(self):
        super().__init__()

        self.title("Calculator")
        self.geometry("300x400")
        self.resizable(False, False)

        self.expression = ""

        self.display_var = tk.StringVar()
        
        style = ttk.Style(self)
        style.configure("TButton", font=("Helvetica", 14), padding=10)
        style.configure("TEntry", font=("Helvetica", 20), padding=10)

        self._create_widgets()

    def _create_widgets(self):
        display = ttk.Entry(
            self, 
            textvariable=self.display_var, 
            font=("Helvetica", 24), 
            justify='right', 
            state='readonly'
        )
        display.grid(row=0, column=0, columnspan=4, sticky="nsew", padx=5, pady=5)

        # --- Button Layout ---
        buttons = [
            '7', '8', '9', '/',
            '4', '5', '6', '*',
            '1', '2', '3', '-',
            '0', '.', '=', '+'
        ]

        row_val = 1
        col_val = 0
        for button_text in buttons:
            action = lambda x=button_text: self.on_button_click(x)
            
            ttk.Button(self, text=button_text, command=action).grid(
                row=row_val, column=col_val, sticky="nsew", padx=2, pady=2
            )
            
            col_val += 1
            if col_val > 3:
                col_val = 0
                row_val += 1
        
        ttk.Button(self, text="C", command=self.on_clear).grid(
            row=row_val, column=0, columnspan=2, sticky="nsew", padx=2, pady=2
        )
        ttk.Button(self, text="DEL", command=self.on_backspace).grid(
            row=row_val, column=2, columnspan=2, sticky="nsew", padx=2, pady=2
        )

        # Make grid cells expand equally
        for i in range(5):
            self.grid_rowconfigure(i, weight=1)
        for i in range(4):
            self.grid_columnconfigure(i, weight=1)

    def on_button_click(self, char):
        if char == '=':
            self.on_equal()
        else:
            self.expression += str(char)
            self.display_var.set(self.expression)

    def on_equal(self):
        try:
            result = str(eval(self.expression))
            self.display_var.set(result)
            self.expression = result
        except (SyntaxError, ZeroDivisionError):
            self.display_var.set("Error")
            self.expression = ""

    def on_clear(self):
        self.expression = ""
        self.display_var.set("")

    def on_backspace(self):
        self.expression = self.expression[:-1]
        self.display_var.set(self.expression)


if __name__ == "__main__":
    app = CalculatorApp()
    app.mainloop()
