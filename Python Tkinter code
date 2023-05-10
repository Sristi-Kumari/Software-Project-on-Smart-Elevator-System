from tkinter import *
from tkinter import messagebox
import os



def register():
    global register_screen
    register_screen = Toplevel(root)
    register_screen.title("Register")
    register_screen.geometry("300x250")

    global username
    global password
    global username_entry
    global password_entry
    username = StringVar()
    password = StringVar()

    Label(register_screen, text="Please enter details below", bg="#6363B8").pack()
    Label(register_screen, text="").pack()
    username_lable = Label(register_screen, text="User_id * ")
    username_lable.pack()
    username_entry = Entry(register_screen, textvariable=username)
    username_entry.pack()
    password_lable = Label(register_screen, text="Password * ")
    password_lable.pack()
    password_entry = Entry(register_screen, textvariable=password, show='*')
    password_entry.pack()
    Label(register_screen, text="").pack()
    Button(register_screen, text="Register", width=10, height=1, bg="#6363B8", command = register_user).pack()



def login():
    global login_screen
    login_screen = Toplevel(root)
    login_screen.title("Login")
    login_screen.geometry("300x250")
    Label(login_screen, text="Please enter details below to login").pack()
    Label(login_screen, text="").pack()

    global username_verify
    global password_verify

    username_verify = StringVar()
    password_verify = StringVar()

    global username_login_entry
    global password_login_entry

    Label(login_screen, text="Username * ").pack()
    username_login_entry = Entry(login_screen, textvariable=username_verify)
    username_login_entry.pack()
    Label(login_screen, text="").pack()
    Label(login_screen, text="Password * ").pack()
    password_login_entry = Entry(login_screen, textvariable=password_verify, show= '*')
    password_login_entry.pack()
    Label(login_screen, text="").pack()
    Button(login_screen, text="Login", width=10, height=1, command = login_verify).pack()



def register_user():

    username_info = username.get()
    password_info = password.get()

    file = open(username_info, "w")
    file.write(username_info + "\n")
    file.write(password_info)
    file.close()

    username_entry.delete(0, END)
    password_entry.delete(0, END)

    Label(register_screen, text="Account created successfully\nProceed with Login", fg="green", font=("calibri", 11)).pack()



def login_verify():
    username1 = username_verify.get()
    password1 = password_verify.get()
    username_login_entry.delete(0, END)
    password_login_entry.delete(0, END)

    list_of_files = os.listdir()
    if username1 in list_of_files:
        file1 = open(username1, "r")
        verify = file1.read().splitlines()
        if password1 in verify:
            login_sucess()

        else:
            password_not_recognised()

    else:
        user_not_found()



def login_sucess():
    global login_success_screen
    login_success_screen = Toplevel(login_screen)
    login_success_screen.title("Success")
    login_success_screen.geometry("200x200")
    Label(login_success_screen, text="Login Success").pack()
    Button(login_success_screen, text="Navigate to the main window",fg="#FFFFA5",bg="#8B8B5A",command=main_window).pack()

def main_window():
    global sty
    global z
    sty=Tk()
    sty.geometry("400x400")
    sty.configure(bg="#FFFFBB")
    sty.title("Main Application Interface")
    def ty():
       msg=messagebox.showinfo("Floor selected successfully","Click Next")
           
    
    Label(sty,text="Select Floor",font=("Calibri",13)).grid(row=4,column=0)
    spin=Spinbox(sty,from_=0,to=15)
    z=spin.get()
    spin.grid(row=4,column=6)
    Button(sty,text="Submit",command=ty).grid(row=4,column=8)
    
    Button(sty,text="Next",command=main2).grid(row=6,column=6)
   
    
    
def main2():
    
    
    Label(sty,text="Select Time slot:",font=("Calibri",13)).grid(row=14,column=0)
    

   
    def uy():
        Label(sty,text="Enter time:",font=("Calibri",13)).grid(row=16,column=0)
        Entry(sty).grid(row=16,column=6)
    #def er():
       
       #rt.config(text=z)
       #if(z==0 or z==1 or z==2 or z==3 or z==4):
            #Label(rt,text="Waiting Time= 3 minutes").place(x=0,y=50)
       
        
    def op():
        global b1    
        mr=messagebox.askquestion("Booking confirmation","Confirm and Proceed?")
        def fre():
            global ty
            ty=Tk()
            ty.title("Feedback Interface")
            ty.geometry("400x400")
            ty.configure(bg="#EEEEC5")
            Label(ty,text="Feedback form").place(x=150,y=0)
            r1=IntVar()
            def ret():
                r2=StringVar()
                def er():
                   m6=messagebox.askquestion("Exit","Thank you for using the application\nDo you want to exit?")
                Label(ty,text="Any Suggestions:").place(x=0,y=100)
                Entry(ty,textvariable=r2).place(x=110,y=100)
                Button(ty,text="Submit",command=er).place(x=80,y=130)
            Label(ty,text="Rate\n(out of 5)").place(x=0,y=30)
            Entry(ty,textvariable=r1).place(x=80,y=40)
            Button(ty,text="Next",command=ret).place(x=50,y=70)
            ty.mainloop()
        global rt
        rt=Tk()
        rt.title("Booking Details")
        rt.geometry("400x400")
        rt.configure(bg="#FFFF7F")
        Label(rt,text="DETAILS REGARDING THE BOOKING").place(x=90,y=0)
        #Label(rt,text="Selected floor").place(x=0,y=30)
        #b1=Button(rt,text="Click to check the floor",command=er).place(x=100,y=30)
        #rt = Label(rt,fg="#45458B")
        #rt.place(x=250,y=30)
        
        Label(rt,text="Waiting Time= 3 minutes").place(x=0,y=50)
        Label(rt,text="You have to arrive to Elevator Number 3 at respected time slot").place(x=0,y=80)
        Label(rt,text="Completed the Journey?\nClick Completed to go to feedback interface").place(x=60,y=200)
        Button(rt,text="Completed",font=("Times New roman",6),command=fre,fg="#535386").place(x=150,y=260)
        
        rt,mainloop()
    def er():
       
       rt.config(text=z)
       Label(rt,text="Your waiting is-").place(x=0,y=50)     
        
      
         
    menubutton = Menubutton(sty, text = "Menu")   
    
    menubutton.menu = Menu(menubutton)  
    menubutton["menu"]= menubutton.menu  
  
    var1 = IntVar()
    var2 = IntVar()
    var3 = IntVar()
    var4= IntVar()
  
    menubutton.menu.add_checkbutton(label = "8am to 10am",
                                variable = var1,command=uy)  
    menubutton.menu.add_checkbutton(label = "10am to 12pm",
                                variable = var2,command=uy)
    menubutton.menu.add_checkbutton(label = "12pm to 3pm",
                                variable = var3,command=uy)
    menubutton.menu.add_checkbutton(label="3pm to 6pm",variable = var4,command=uy)
    menubutton.grid(row=14,column=6)
    Button(sty,text="Confirm Booking",command=op).grid(row=20,column=4)
    
  

def password_not_recognised():
    global password_not_recog_screen
    password_not_recog_screen = Toplevel(login_screen)
    password_not_recog_screen.title("Success")
    password_not_recog_screen.geometry("150x100")
    Label(password_not_recog_screen, text="Invalid Password ").pack()
    Button(password_not_recog_screen, text="OK", command=delete_password_not_recognised).pack()




def user_not_found():
    global user_not_found_screen
    user_not_found_screen = Toplevel(login_screen)
    user_not_found_screen.title("Success")
    user_not_found_screen.geometry("150x100")
    Label(user_not_found_screen, text="User Not Found").pack()
    Button(user_not_found_screen, text="OK", command=delete_user_not_found_screen).pack()



def delete_login_success():
    login_success_screen.destroy()


def delete_password_not_recognised():
    password_not_recog_screen.destroy()


def delete_user_not_found_screen():
    user_not_found_screen.destroy()


def main_account_screen():
    global root
    root = Tk()
    root.geometry("1000x1000")
    root.title("Smart Elevator System")
    root.configure(bg='#F0F0F8')
    bg= PhotoImage(file="login.png")
    l5=Label(root,image=bg)
    l5.pack(side=BOTTOM,anchor="nw")
    l1=Label(root,text="Welcome To Smart Elevator System",font=("TIMES NEW ROMAN",30,'bold'),fg='red')
    l1.pack()
    Label(text="Sign in",bg="#5C5CAC",fg="white",width="300", height="2", font=("Calibri", 13)).pack()
    Label(text="").pack()
    Button(text="Login",height="2", width="30", command = login).pack()
    Label(text="").pack()
    Label(text="Don't have an account?\nCreate account to proceed").pack()
    Button(text="Create Account", height="2", width="30", command=register).pack()
    photo=PhotoImage(file="sample.png")
    label=Label(root,image=photo)
    label.pack(side=BOTTOM,anchor="se")

    root.mainloop()

main_account_screen()
