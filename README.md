from tkinter import *
from tkinter import messagebox
window =Tk()
def submit():
    messagebox.showinfo("Submitted", "Registration Successful")

window.title("Registration Form")
title = Label(window, text="REGISTRATION FORM", font=("Times new roman", 16))
title.grid(row=0, column=0)

l1=Label(window, text="Full Name").grid(row=1)
l2=Label(window, text="Email").grid(row=2)
l3=Label(window, text="Gender").grid(row=3)
l4=Label(window, text="Country").grid(row=4)
l5=Label(window, text="Programming Language").grid(row=5)

e1=Entry(window).grid(row=1, column=1)
e2=Entry(window).grid(row=2, column=1)

gender = StringVar()
r1=Radiobutton(window, text="Male", variable=gender, value="Male").grid(row=3, column=1)
r2=Radiobutton(window, text="Female", variable=gender, value="Female").grid(row=3, column=2)

countries = ["India", "USA", "UK", "Australia", "Canada"]
country = StringVar()
country.set(countries[0])  # default value
o1=OptionMenu(window, country, *countries).grid(row=4, column=1)

language = StringVar()
c1=Checkbutton(window,text="Java",variable=language).grid(row=5, column=1)
c2=Checkbutton(window,text="python",variable=language).grid(row=5, column=2)
b1=Button(window,text='Submit', command=submit,bg='red',fg='white',font=('Times new roman',10)).grid(row=6, pady=1)
window.mainloop()
