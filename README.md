# Language-translator-from  compiler import *
from translate import Translator 

#create a window 
Window =Tk()
Window.title("language translator")

# Add a grid to window 
Mainframe = Frame(window)
Mainframe.grid(column=0,row=0)
#mainframe.columnconfigure(0,weight=1)
#mainframe.rowconfigure(0,weight=1)
Mainframe.pack(pady =100,padx = 100)

#variables to set languages
Lan1 = Stringvar(window)
Lan2=stringvar(window)

#funtion which translates the given text
def trans():
    translator =Translator(from_lan = lan1.get(), to_lang=lan2.get())
    translation =translator.translate(var.gett())
    Var1.set(translation)

#select language
Choice = {"ENGLISH","HINDI"}
Lan1menu = OptionMenu( mainframe, lan1,*choice)
Label(mainframe,text="select language").grid(row =0,column=1)
Lan1menu.grid(row =1,column=1)


Lan2menu = OptionMenu( mainframe ,lan2,*choice)
Label(mainframe, text="select language").grid(row= 0,column =1)


#input text field 
Label(mainframe, text = "enter text").grid(row=2,column=0)
Var =StringVar()
Textbox = Entry(mainframe ,textvariable = var).grid(row=2,column=1)

#output text field 
Label(mainframe, text ="output").grid(row=2,column=2)
Var1 =StringVar()
Textbox = entry(mainframe, textvariable = var1).grid(row=2,column=3)

Button =Button(mainframe,text= 'translate', command = trans).grid(row=3,column=1, columnspan=3)


Window.mainloop()
