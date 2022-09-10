from tkinter import*

def btnClick(numbers):
    global operator
    operator=operator + str(numbers)
    text_Input.set(operator)
    
def btnClearDisplay():
    global operator
    operator=""
    text_Input.set("")
    
def btnEqualsInput():
    global operator
    sumup=str(eval(operator))
    text_Input.set(sumup)
    operator=""
    


cal = Tk()
cal.title("Cal")
operator=""
text_Input =StringVar()

txtDisplay = Entry(cal,font=('arial',20,'bold'), textvariable=text_Input, bd=40, insertwidth=10,
                   bg="White", justify='right').grid(columnspan=20)

btn7=Button(cal,padx=20,pady=20 ,bd=15, fg="White", font=('arial',20,'bold'),
            text="7",bg="Black", command=lambda:btnClick(7)).grid(row=1,column=0)

btn8=Button(cal,padx=20,pady=20 ,bd=15, fg="White", font=('arial',20,'bold'),
            text="8",bg="Black", command=lambda:btnClick(8)).grid(row=1,column=1)

btn9=Button(cal,padx=20,pady=20 ,bd=15, fg="White", font=('arial',20,'bold'),
            text="9",bg="Black", command=lambda:btnClick(9)).grid(row=1,column=2)

Addition=Button(cal,padx=20,pady=20 ,bd=15, fg="White", font=('arial',20,'bold'),
            text="+",bg="Black", command=lambda:btnClick("+")).grid(row=1,column=3)
#====================================================================================================================

btn4=Button(cal,padx=20,pady=20 ,bd=15, fg="White", font=('arial',20,'bold'),
            text="4",bg="Black", command=lambda:btnClick(4)).grid(row=2,column=0)

btn5=Button(cal,padx=20,pady=20 ,bd=15, fg="White", font=('arial',20,'bold'),
            text="5",bg="Black", command=lambda:btnClick(5)).grid(row=2,column=1)

btn6=Button(cal,padx=20,pady=20 ,bd=15, fg="White", font=('arial',20,'bold'),
            text="6",bg="Black", command=lambda:btnClick(6)).grid(row=2,column=2)

Subtraction=Button(cal,padx=20,pady=20 ,bd=15, fg="White", font=('arial',20,'bold'),
            text="-",bg="Black", command=lambda:btnClick("-")).grid(row=2,column=3)
#====================================================================================================================
btn1=Button(cal,padx=20,pady=20 ,bd=15, fg="White", font=('arial',20,'bold'),
            text="1",bg="Black", command=lambda:btnClick(1)).grid(row=3,column=0)

btn2=Button(cal,padx=20,pady=20 ,bd=15, fg="White", font=('arial',20,'bold'),
            text="2",bg="Black", command=lambda:btnClick(2)).grid(row=3,column=1)

btn3=Button(cal,padx=20,pady=20 ,bd=15, fg="White", font=('arial',20,'bold'),
            text="3",bg="Black", command=lambda:btnClick(3)).grid(row=3,column=2)

Multiplication=Button(cal,padx=20,pady=20 ,bd=15, fg="White", font=('arial',20,'bold'),
            text="*",bg="Black", command=lambda:btnClick("*")).grid(row=3,column=3)
#====================================================================================================================

btn0=Button(cal,padx=20,pady=20 ,bd=15, fg="White", font=('arial',20,'bold'),
            text="0",bg="Black", command=lambda:btnClick(0)).grid(row=4,column=0)

btnClear=Button(cal,padx=20,pady=20 ,bd=15, fg="White", font=('arial',20,'bold'),
            text="c",bg="Black",command=btnClearDisplay).grid(row=4,column=1)

btnEquals=Button(cal,padx=20,pady=20 ,bd=15, fg="White", font=('arial',20,'bold'),
            text="=",bg="Black",command=btnEqualsInput).grid(row=4,column=2)

Division=Button(cal,padx=20,pady=20 ,bd=15, fg="White", font=('arial',20,'bold'),
            text="/",bg="Black", command=lambda:btnClick("/")).grid(row=4,column=3)
#====================================================================================================================

cal.mainloop()


 

