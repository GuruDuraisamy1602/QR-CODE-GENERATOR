## QR CODE GENERATOR
## OBJECTIVE OF THE PROJECT
This project is entitled as QR CODE GENERATOR. It creates a QR code for a 
particular string or URL.to create a QR code generator using python the GUI of the 
project we are going to use the tkinter module and its built function. For creating a 
QR code we are going to use the pyqr code library. the user will have the entry field 
to to enter the URL or the string and a QR code will be generated accordingly and 
will be save in the system. It is an application that takes in a URL or a string and 
creates a QR code for it. Here we can save the generated QR code as an image with 
the .png extension.
## CODE
Certainly! It seems the code got cut off. Here's the continuation and completion:

```python
Subject = StringVar()

SubEntry = Entry(f, textvariable=Subject, width=50, font=("gothic", 12))
SubEntry.grid(row=0, column=0, columnspan=5, sticky=N+S+W+E)
SubEntry.insert(END, "Enter subject here")
SubEntry.bind("<FocusOut>", repopulate_defaults)
SubEntry.bind("<FocusIn>", clear_widget)

Name = StringVar()
nameEntry = Entry(f, textvariable=Name, width=50, font=("gothic", 12))
nameEntry.grid(row=1, column=0, columnspan=5, sticky=N+S+W+E)
nameEntry.insert(0, "Enter filename here")
nameEntry.bind("<FocusOut>", repopulate_defaults)
nameEntry.bind("<FocusIn>", clear_widget)

f2 = Frame(window)
f2.grid(row=2, column=0, sticky=N+S+W+E)

S1 = Button(f2, text="Qr code", width=9, command=generate, font=("Helvetica", 12))
S1.grid(row=0, column=0, sticky=N+S+W+E)

S1 = Button(f2, text="Save", width=9, command=dummy, font=("Helvetica", 12))
S1.grid(row=0, column=1, sticky=N+S+W+E)

S1 = Label(f2, text=" ", width=3)
S1.grid(row=0, column=2, sticky=N+S+W+E)

S1 = Button(f2, text="Bar code", width=9, command=bargenerate, font=("Helvetica", 12))
S1.grid(row=0, column=3, sticky=N+S+W+E)

S1 = Button(f2, text="Save", width=9, command=brsave, font=("Helvetica", 12))
S1.grid(row=0, column=4, sticky=N+S+W+E)

f3 = Frame(window)
f3.grid(row=3, column=0, columnspan=2, sticky=N+S+W+E)

S1 = Button(f3, text="Small", width=4, command=lambda: setsize(8), font=("Helvetica", 12))
S1.grid(row=0, column=0, sticky=N+S+W+E)

S1 = Button(f3, text="Medium", width=7, command=lambda: setsize(10), font=("Helvetica", 12))
S1.grid(row=0, column=1, sticky=N+S+W+E)

S1 = Button(f3, text="Large", width=6, command=lambda: setsize(16), font=("Helvetica", 12))
S1.grid(row=0, column=2, sticky=N+S+W+E)

f4 = Frame(window)
f4.grid(row=4, column=0, columnspan=2, sticky=N+S+W+E)

saveB = Button(f4, text="PNG", width=9, command=save, font=("Helvetica", 12))
saveB.grid(row=1, column=0, sticky=N+S+W+E)

saveC = Button(f4, text="SVG", width=9, command=svg, font=("Helvetica", 12))
saveC.grid(row=1, column=1, sticky=N+S+W+E)

imageLabel = Label(window)
imageLabel.grid(row=5, column=0, sticky=N+S+W+E)

subLabel = Label(window, text="")
subLabel.grid(row=6, column=0, sticky=N+S+W+E)

Rows = 6
Columns = 4

for row in range(Rows + 1):
    window.grid_rowconfigure(row, weight=1)

for col in range(Columns + 1):
    window.grid_columnconfigure(col, weight=1)

window.mainloop()
```

This should complete the program. Please note that there might still be some improvements and adjustments needed based on your specific requirements and the actual behavior you want from the GUI.
