# weight-converter
from tkinter import *
from tkinter import ttk
def calculate(*args):
	try:
		value = int(gram.get())
		Kgram.set(1000*value)
	except:
		pass
root = Tk()
root.title('Gram to Kilogram')
root.geometry('390x100+120+150')
gram = StringVar()
Kgram = StringVar()
g_get = Entry(root, textvariable=gram)
g_get.grid(row=0, column=4, columnspan=5, padx=32, pady=7)
g_get.configure(bg = '#00ffff')
g_get.configure(fg='Black')
Label(root, text='Gram').grid(row=0, column=16, padx=2, pady=4)
Label(root, text="Is equivalent to: ").grid(row=1, column=0, padx=2, pady=2)
kg_get = Label(root, textvariable=Kgram)
kg_get.grid(row=1, column=4, columnspan = 5, padx=2, pady=3)
Label(root, text='Kilogram').grid(row=1, column=16, padx=2, pady=4)
lock = Button(root, text='calculate', command=calculate)
lock.grid(row=2, column=16, columnspan=18, padx=2, pady=4)
g_get.focus()
root.bind("<Return>", calculate)
root.mainloop()


