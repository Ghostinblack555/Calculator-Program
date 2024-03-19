import tkinter as tk
def button_click(symbol):
    current = entry_display.get()
    entry_display.delete(0, tk.END)
    entry_display.insert(tk.END, current + symbol)
def clear_display():
    entry_display.delete(0, tk.END)
def calculate_result():
    try:
        result = eval(entry_display.get())
        entry_display.delete(0, tk.END)
        entry_display.insert(tk.END, str(result))
    except:
        entry_display.delete(0, tk.END)
        entry_display.insert(tk.END, "Error")
root = tk.Tk()
root.title("CALCULATOR")
entry_display = tk.Entry(root, width=30, font=('Arial', 20), justify=tk.RIGHT)
entry_display.grid(row=0, column=0, columnspan=4)
buttons = [
    ('7', 1, 0), ('8', 1, 1), ('9', 1, 2), ('/', 1, 3),
    ('4', 2, 0), ('5', 2, 1), ('6', 2, 2), ('*', 2, 3),
    ('1', 3, 0), ('2', 3, 1), ('3', 3, 2), ('-', 3, 3),
    ('0', 4, 0), ('.', 4, 1), ('=', 4, 2), ('+', 4, 3)
]

for (text, row, col) in buttons:
    button = tk.Button(root, text=text, width=5, height=2, font=('Arial', 14),
                       command=lambda t=text: button_click(t))
    button.grid(row=row, column=col)
button_clear = tk.Button(root, text='C', width=5, height=2, font=('Arial', 14),
                         command=clear_display)
button_clear.grid(row=5, column=0)
button_calculate=tk.Button(root, text='Ans', width=5, height=2, font=('Arial', 14),
                        command=calculate_result)
button_calculate.grid(row=5, column=1)
root.mainloop()
