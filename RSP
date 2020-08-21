from tkinter import *
from tkinter import messagebox
from random import *
from time import *



pc_score = 0
user_score = 0
pc_figur = ""
user_figur = ""


def stone():
     global user_figur
     Kbut["bg"]="green"
     Nbut["bg"]="white"
     Bbut["bg"]="white" 
     user_figur = "камень"
     PCbut["state"] = "normal"


def scissors():
     global user_figur
     Kbut["bg"]="white"
     Nbut["bg"]="green"
     Bbut["bg"]="white" 
     user_figur = "ножницы"
     PCbut["state"] = "normal"    


def paper():
     global user_figur
     Kbut["bg"]="white"
     Nbut["bg"]="white"
     Bbut["bg"]="green" 
     user_figur = "бумага"
     PCbut["state"] = "normal"     


def go():
      global pc_figur, user_figur, user_score, pc_score
      t4["text"] = "выбор pc - "
      for i in range(30):
           ran = randint(1,4)
           if ran == 1:
                pc_figur = "камень"
           if ran == 2:
                pc_figur = "ножницы"
           if ran == 3:
                pc_figur = "бумага"

           t4["text"] = "выбор pc - " + pc_figur
           t4.update()
           sleep(0.1)

      if pc_figur == user_figur:
           messagebox.showinfo("result", "Drow")

      else:
           if pc_figur == "камень" and user_figur == "ножницы":
                pc_score += 1
                messagebox.showinfo("result", "PC Победил")
           if pc_figur == "камень" and user_figur == "бумага":
                user_score += 1
                messagebox.showinfo("result", "user Победил")

           if pc_figur == "ножницы" and user_figur == "бумага":
                pc_score += 1
                messagebox.showinfo("result", "PC Победил")
           if pc_figur == "ножницы" and user_figur == "камень":
                user_score += 1
                messagebox.showinfo("result", "user Победил")

           if pc_figur == "бумага" and user_figur == "камень":
                pc_score += 1
                messagebox.showinfo("result", "PC Победил")
           if pc_figur == "бумага" and user_figur == "ножницы":
                user_score += 1
                messagebox.showinfo("result", "user Победил")

           t5["text"] = "Игрок - " + str(user_score)
           t6["text"] = "PC - " + str(pc_score)

      PCbut["state"] = "disabled"


root = Tk()
root.title("Камень,Ножницы,Бумага")

t1 = Label(root, text="Камень, ножницы, бумага", fg="red")
t1.grid(row=0, column=1)
t2 = Label(root, text="Выбор игрока", fg="green")
t2.grid(row=1, column=1)

Kbut=Button(root, text="Камень", command = stone)
Kbut.grid(row=2, column=0)
Nbut=Button(root, text="Ножницы", command = scissors)
Nbut.grid(row=2, column=1)
Bbut=Button(root, text="Бумага", command = paper)
Bbut.grid(row=2, column=2)

t3 = Label(root, text="Выбор Компьютера", fg="blue")
t3.grid(row=3, column=1)
PCbut=Button(root, text="Сгенерировать", command = go)
PCbut["state"] = "disabled"
PCbut.grid(row=4, column=1)

t4 = Label(root, text="выбор pc - 0", fg="red")
t4.grid(row=6, column=1)

t5 = Label(root, text="Игрок - 0", fg="green")
t5.grid(row=7, column=0)

t6 = Label(root, text="PC - 0", fg="blue")
t6.grid(row=7, column=2)
root.mainloop()
