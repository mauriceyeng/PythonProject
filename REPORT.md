# PythonProject
INT 213 Project 2020-2021


PROJECT REPORT OF INT 213
(Term 2020-2021)
SCHOOL OF COMPUTER SCIENCE AND ENGINEERING

 



KIDS LEARNING GAME


GITHUB LINK: https://github.com/mauriceyeng/PythonProject.git
SUBMMITED BY:
NAME	REG NO	ROLL NO	SECTION
MAURICE YENGKHOM	11907009	59	K19AW
PRIYOJIT SINGHA	12002212	37	K19AW
RAJ DUTTA	12005560	35	K19AW







Acknowledgements

I have taken efforts in this project. However, it would not have been possible without the kind support and help of our teacher Ma’am Pooja Rana and individuals. I would like to extend my sincere thanks to all of them.
I would like to express my gratitude towards my parents & member of our project for their kind co-operation and encouragement which help us in completion of this project.
I would like to express my special gratitude and thanks to our teacher Ma’am Pooja Rana for giving us such attention, time and opportunity.

My thanks and appreciations also go to my colleague in developing the project and people who have willingly helped us out with their abilities.











Introduction:
Games and education have a very important in our life. Playing games that give some knowledge and improve our memory power.
Python is a powerful, expressive programming language that's easy to learn and fun to use! But books about learning to program in Python can be kind of dull and boring, and that's no fun for anyone.
Python for Kids brings Python to life and brings something into the world of programming. This will guide you through the basics as you experiment with unique (and often hilarious) example programs that feature ravenous monsters, secret agents, thieving ravens, and more. New terms are defined; code is coloured, dissected, and explained; and quirky, full-colour illustrations keep things on the lighter side.
 By the end of the project we have done one programmed one complete game is quiz for kids learning game with the help of Python

As you strike out on your programming adventure, we have done how to:
•	Use fundamental data structures like lists, tuples, and maps
•	Organize and reuse your code with functions and modules
•	Use control structures like loops and conditional statements
•	Create games, animations, and other graphical wonders with tkinter

Prospects of kids learning game in Python for Kids:

Python Programming for Kids can open a lot of career options for kids in the future. With many advanced fields using Python, a lot of career opportunities have opened now and will continue to do so in the future. Some notable ones are:
Data Scientist:
They are a highly skilled set of professionals who not just need to know how to work with data but should know statistical methods and algorithms.

Data Analyst:
Data analysts analyse various kinds of data and come up with data-driven insights. They help businesses make decisions based on their study and findings.

Python Programmer:
They are professionals who develop different applications using Python.
Game Developer:

The gaming industry combines creativity with innovation. While C++, Java, etc. are used in gaming, Python is also quite commonly used to develop games. Python has libraries that support game development.
Python Programming advantages are numerous. Many more options open to Skilled Python Professionals. Python can take your kid a step closer to his lucrative future career.




The Importance Of Kids Learning Games

Educational Learning is taking a new dimensional approach by incorporating the concept of games. With the development of modern technology, there is an array of applications which help impart knowledge. The current environment of digital games and applied sciences into learning environment has benefited both the teaching of educators and the learning of students.
The concept of Game-Based Learning (GBL) can be successfully used to achieve better methods for both learning and teaching. It basically means incorporating games in your medium of instruction. One of the prime challenges educators face is of teaching a huge group of students, all of whom are unique and have totally different personalities, wave-length of learning and capabilities. With great expectations, students get an opportunity to work on various educational games along with rewards and surprise elements which help to keep their interest in learning.
Game-based learning plays a vital role in teaching by offering the opportunity for students to collaborate, communicate, interact and work in teams with each other. Strategy-based games enhance the functioning of the brain, inspire children to learn new things, develop their skills and build an emotional connect to learn the subject matter. The feature of receiving feedback immediately after playing a game gives insight on how to improve the performance in a positive way. Incorporating the educational learning objectives along with the curriculum gives a completely new form to learning.



Some of the important benefits of Kids educational games are as below:
•	Increases Memory
•	Strategic Thinking
•	Hand-Eye Coordination
•	Skill-Building
As mentioned, there are many reasons why educational games can be beneficial for children and their development. It has to be positively embedded in modern education to give children the maximum benefit of learning.

Work Division:
Maurice Yengkhom: Colours Game
Priyojit Singha: Number’s Game
Raj Dutta: ABCs Game



Conclusion:
Educational games are vital to interactively achieve new goals and objectives for learning. Let game-based learning be incorporated for the betterment of children’s education and the quality of skill and knowledge they gain; along with the enhancement of the brain, concentration, memory and creative awareness



PYTHON-CODE
from tkinter import *
import random
from tkinter import ttk, font, colorchooser, filedialog, messagebox

root = Tk()
root.geometry('600x500')
root.minsize(600, 500) #min width,height
root.maxsize(600, 500)
root.geometry("{}x{}+{}+{}".format(600, 500, int((root.winfo_screenwidth()/2) - (600/2)), int((root.winfo_screenheight()/2) - (500/2))))

root.title("KIDS LEARNING GAME")
main_icon = PhotoImage(file = "icons/main_icon.png")
root.iconphoto(False, main_icon)

heading_frame = Frame(root, bg='white')
heading_frame.pack(fill=BOTH,expand=True)

heading1 = Label(heading_frame, text=" KIDS LEARNING GAME\n",font=("Arial Rounded MT Bold", 26),bg='white',fg='black')
heading1.pack()

main_icon_label= Label(heading_frame, image=main_icon,bg='white')
main_icon_label.pack()

heading2 = Label(heading_frame, text="\n\nProject Submitted By: \n\nMaurice Yengkhom\nPriyojit Singha \nRaj Dutta\n\n\n",font=("", 10),bg='white',fg='black')
heading2.pack()

def colors_game():
    root1.destroy()
    global root2
    root2=Tk()
    root2.tkraise()       #To bring the window in focus
    root2.focus_force()   #To bring the window in focus
    root2.title("KIDS LEARNING GAME")
    root2.geometry('600x500')
    root2.minsize(600, 500) #min width,height
    root2.maxsize(600, 500)
    root2.geometry("{}x{}+{}+{}".format(600, 500, int((root2.winfo_screenwidth()/2) - (600/2)), int((root2.winfo_screenheight()/2) - (500/2))))
    main_icon = PhotoImage(file = "icons/main_icon.png")
    root2.iconphoto(False, main_icon)
    root2.configure(background='white')

    Label(root2,text="Welcome to COLORs GAME",font=("Arial 93",17),fg="Red",bg="White").place(relx=0.5,y=20,anchor='center')
    Label(root2,text="Type in the colour of the words, and not the word text!",font=("Arial 93",12),fg="White",bg="Orange").place(relx=0.5,y=50,anchor='center')

    #LOGIC OF GAME STARTS
    
    colours = ['Red','Blue','Green','Pink','Black','Yellow','Orange','Cyan','Purple','Brown'] # list of possible colour
    global score              # variables 'score' and 'timeleft' are declared globally
    global timeleft
    score = 0
    timeleft = 30             # the game time left, initially 30 seconds
      
    def startGame(event):     # function that will start the game
        if timeleft == 30: 
            countdown()       # start the countdown timer
        nextColour()          # run the function to choose the next colour 
      
    def nextColour():         # Function to choose and display the next colour
        global score          # variables 'score' and 'timeleft' are declared globally
        global timeleft 
      
        if timeleft > 0:      # if a game is currently in play 
            e.focus_set()     # make the text entry box active.  
            if e.get().lower() == colours[1].lower(): # if the colour typed is equal to the colour of the text
                score += 1
            e.delete(0,END)   # clear the text entry box
            random.shuffle(colours) 
            label.config(fg = str(colours[1]), text = str(colours[0])) # change the colour to type, by changing the text and the colour to a random colour value
            scoreLabel.config(text = "Score: " + str(score))           # update the score
        
    def countdown():          # Countdown timer function
        global timeleft 
        if timeleft > 0:      # if a game is in play 
            timeleft -= 1     # decrement the timer 
            timeLabel.config(text = "Time left: " + str(timeleft))     # update the time left label                     
            timeLabel.after(1000, countdown)                           # run the function again after 1 second.
        else:
            result = "Game Over! You scored "+ str(score)
            ok = messagebox.showinfo("Finish", result)
            if ok:
                root2.destroy()

    #LOGIC OF GAME ENDS
            
    scoreLabel = Label(root2, text = "Press enter to start", font = ('Helvetica', 12),bg='white') #a score label
    scoreLabel.place(relx=0.5,y=150,anchor='center')
    timeLabel = Label(root2, text = "Time left: " + str(timeleft), font = ('Helvetica', 12),bg='white') #time left label
    timeLabel.place(relx=0.5,y=200,anchor='center')
    label = Label(root2, font = ('Helvetica', 60),bg='white')          #label for displaying the colours
    label.place(relx=0.5,y=280,anchor='center')
  
    e = Entry(root2, font = ('Helvetica', 22))                         #text entry box for typing in colours 
    root2.bind('<Return>', startGame)  # run the 'startGame' function, when the enter key is pressed
    e.focus_set()              # set focus on the entry box 
    e.place(relx=0.5,y=450,anchor='center')

def numbers_game():
    root1.destroy()
    global root2
    root3=Tk()
    root3.tkraise()       #To bring the window in focus
    root3.focus_force()   #To bring the window in focus
    root3.title("KIDS LEARNING GAME")
    root3.geometry('600x500')
    root3.minsize(600, 500) #min width,height
    root3.maxsize(600, 500)
    root3.geometry("{}x{}+{}+{}".format(600, 500, int((root3.winfo_screenwidth()/2) - (600/2)), int((root3.winfo_screenheight()/2) - (500/2))))
    main_icon = PhotoImage(file = "icons/main_icon.png")
    root3.iconphoto(False, main_icon)
    root3.configure(background='white')

    Label(root3,text="NUMBER GAME",font=("Arial 93",17),fg="Red",bg="White").place(relx=0.5,y=20,anchor='center')
    Label(root3,text="Enter the correct answer!",font=("Arial 93",12),fg="White",bg="Orange").place(relx=0.5,y=50,anchor='center')

    global no
    no=0
    #LOGIC OF GAME STARTS    

    question_list=['2+7 = ','1,3,5,7,9,_ What comes after 9?','2,4,6,8,_ What comes after 8?','2,12,45,76,1 Which is the greatest number?']
    option_list=[['9','8','6'],['10','11','12'],['9','11','10'],['12','45','76']]
    answers=[1,2,3,3]
    
    q_label= Label(root3,text=question_list[no],font=("Arial 93",17),fg="Red",bg="White")
    q_label.place(relx=0.5,y=100,anchor='center')
    
    def a1():
        global no
        no+=1
            
        if(var.get()==answers[no-1]):
            messagebox.showinfo("Correct answer!","You chose the right answer") #alert box
           
        else:
            answer = option_list[no-1][answers[no-1]-1]
            to_show = " The correct answer is " + answer + " !"
            messagebox.showinfo("Wrong answer!", to_show)   #alert box

        if(no!=4):
            q_label.config(text=str(question_list[no]))
            r1.config(text=str(option_list[no][0]))
            r2.config(text=str(option_list[no][1]))
            r3.config(text=str(option_list[no][2]))
        else:
            ok = messagebox.showinfo("Finish", "Game Over!")
            if ok:
                root3.destroy()
        
    var=IntVar(root3)

    Label(root3,text="choose the correct option",bg='white').place(relx=0.5,y=150,anchor='center')
        
    r1=Radiobutton(root3,text=option_list[no][0],value=1,bg='white',variable=var)
    r1.place(relx=0.5,y=200,anchor='center')
    r2=Radiobutton(root3,text=option_list[no][1],value=2,bg='white',variable=var)
    r2.place(relx=0.5,y=250,anchor='center')
    r3=Radiobutton(root3,text=option_list[no][2],value=3,bg='white',variable=var)
    r3.place(relx=0.5,y=300,anchor='center')     
        
    b1=Button(root3,text="Next",bg="black",font=("Calibri", 20),fg="white",cursor="hand2",command=a1)
    b1.place(relx=0.5,y=380,anchor="center")    

    
def abcs_game():
    root1.destroy()
    global root2
    root3=Tk()
    root3.tkraise()       #To bring the window in focus
    root3.focus_force()   #To bring the window in focus
    root3.title("KIDS LEARNING GAME")
    root3.geometry('600x500')
    root3.minsize(600, 500) #min width,height
    root3.maxsize(600, 500)
    root3.geometry("{}x{}+{}+{}".format(600, 500, int((root3.winfo_screenwidth()/2) - (600/2)), int((root3.winfo_screenheight()/2) - (500/2))))
    main_icon = PhotoImage(file = "icons/main_icon.png")
    root3.iconphoto(False, main_icon)
    root3.configure(background='white')

    Label(root3,text="ABC GAME",font=("Arial 93",17),fg="Red",bg="White").place(relx=0.5,y=20,anchor='center')
    Label(root3,text="Enter the correct answer!",font=("Arial 93",12),fg="White",bg="Orange").place(relx=0.5,y=50,anchor='center')

    global no
    no=0
    #LOGIC OF GAME STARTS    

    question_list=['How many vowels are there in the word "Telephone"','Choose an alphabet that comes after "H" but before "L" ','Choose a word that starts with C and ends with A']
    option_list=[['2','3','4'],['M','G','J'],['CLASH','CAMERA','CRANE']]
    answers=[3,3,2]
    
    q_label= Label(root3,text=question_list[no],font=("Arial 93",17),fg="Red",bg="White")
    q_label.place(relx=0.5,y=100,anchor='center')
    
    def a1():
        global no
        no+=1
            
        if(var.get()==answers[no-1]):
            messagebox.showinfo("Correct answer!","You chose the right answer") #alert box
           
        else:
            answer = option_list[no-1][answers[no-1]-1]
            to_show = " The correct answer is " + answer + " !"
            messagebox.showinfo("Wrong answer!", to_show)   #alert box

        if(no!=3):
            q_label.config(text=str(question_list[no]))
            r1.config(text=str(option_list[no][0]))
            r2.config(text=str(option_list[no][1]))
            r3.config(text=str(option_list[no][2]))
        else:
            ok = messagebox.showinfo("Finish", "Game Over!")
            if ok:
                root3.destroy()
        
    var=IntVar(root3)

    Label(root3,text="choose the correct option",bg='white').place(relx=0.5,y=150,anchor='center')
        
    r1=Radiobutton(root3,text=option_list[no][0],value=1,bg='white',variable=var)
    r1.place(relx=0.5,y=200,anchor='center')
    r2=Radiobutton(root3,text=option_list[no][1],value=2,bg='white',variable=var)
    r2.place(relx=0.5,y=250,anchor='center')
    r3=Radiobutton(root3,text=option_list[no][2],value=3,bg='white',variable=var)
    r3.place(relx=0.5,y=300,anchor='center')     
        
    b1=Button(root3,text="Next",bg="black",font=("Calibri", 20),fg="white",cursor="hand2",command=a1)
    b1.place(relx=0.5,y=380,anchor="center")

def main_game():
    root.destroy()
    global root1
    root1=Tk()
    root1.focus_force() #To bring the window in focus
    root1.title("KIDS LEARNING GAME")
    root1.geometry('600x500')
    root1.minsize(600, 500) #min width,height
    root1.maxsize(600, 500)
    root1.geometry("{}x{}+{}+{}".format(600, 500, int((root1.winfo_screenwidth()/2) - (600/2)), int((root1.winfo_screenheight()/2) - (500/2))))
    main_icon = PhotoImage(file = "icons/main_icon.png")
    root1.iconphoto(False, main_icon)
    root1.configure(background='white')
    Label(root1,text="KIDS LEARNING GAME",font=("Arial 93",17),fg="Red",bg="White").place(relx=0.5,y=20,anchor='center')
    Label(root1,text="Choose The Game You Want To Play",font=("Arial 93",17),fg="White",bg="Orange").place(relx=0.5,y=50,anchor='center')

    colors_icon = PhotoImage(file = "icons/colors.png")
    numbers_icon = PhotoImage(file = "icons/numbers.png")
    abcs_icon = PhotoImage(file = "icons/abcs.png")
    
    colors_icon_label= Label(root1, image=colors_icon,bg='white').place(relx=0.30,y=150,anchor='center')
    numbers_icon_label= Label(root1, image=numbers_icon,bg='white').place(relx=0.30,y=250,anchor='center')
    abcs_icon_label= Label(root1, image=abcs_icon,bg='white').place(relx=0.30,y=350,anchor='center')

    
    Button(root1,text=" COLORS",font=("Arial",16),fg="black",bg="lime",compound="center",width=15,height=1,cursor="hand2", command=colors_game).place(relx=0.60,y=150,anchor='center')
    Button(root1,text=" NUMBERS",font=("Arial",16),fg="black",bg="orange",compound="center",width=15,height=1,cursor="hand2", command=numbers_game).place(relx=0.60,y=250,anchor='center')
    Button(root1,text=" ABCs",font=("Arial",16),fg="black",bg="yellow",compound="center",width=15,height=1,cursor="hand2", command=abcs_game).place(relx=0.60,y=350,anchor='center')
    
    
    root1.mainloop()
    
button1 = Button(heading_frame,text="Proceed to Game",command=main_game,compound="center",bg="black",font=("Calibri", 20),fg="white",cursor="hand2")
button1.pack()

root.mainloop()
