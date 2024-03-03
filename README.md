print("Create your bank account!")

d={} #creating empty dictionary

#getting input for creating account

name=input("Enter your name : ")

email=input("Create your email : ")

pwd=input("Create your password : ")

#assigning values to the dictionary

d["Name"]=name

d["Email"]=email

d["Password"]= pwd

d["Amount"]=0

print("Account Created!")

print(d)

#creating while loop for continuous bank operations until you exit

i=0

while i <1:

    var=int(input("Choose the operation that you want to perform!! \n1. Deposit amount \n2. Withdraw amount \n3. View account balance \n4. Change Password \n5. Simple Interest calculator \n6. Compound Interest calculator \n7. Exit \nEnter your option : "))

    if var==1:

        val=int(input("Enter the amount you want to deposit : "))

        d["Amount"]+=val

        print("The amount of",val ,"rs has been successfully deposited in your account!")

        print()

    elif var==2:

        val2=int(input("Enter the amount you want to withdraw : "))

        if d["Amount"] > val2:   #making sure withdrawing amount is less than that of bank balance

             d["Amount"]=d["Amount"] - val2

             print("The amount of",val2 ,"rs has been successfully withdrawed from your account!")

             print("Remaining amount in your account : ",d["Amount"], "rs")

             print()

        else :

             print("You don't have",val2 ,"rs in your account")

             print("Remaining amount in your account : ",d["Amount"], "rs")

             print()

    elif var==3:

        print("Your account balance is",d["Amount"] ,"rs")

        print()

    elif var==4:

        pwd1=input("Enter your current Password :")

        if pwd1==d["Password"]:  

            pwd2=input("Enter your new password :")

            d["Password"]=pwd2

            print("Your password has been changed!")

            print()

        else:

            print("Wrong password! Please try again..")

            print()

    elif var==5:

        print("Fill the below details to calculate the Simple Interest amount!")

        pr=int(input("Enter Principal Amount : "))

        rate=int(input("Enter Rate of Interest : "))

        time=int(input("Enter Time (in years) : "))

        SI=(pr*rate*time)/100

        print("The Simple Interest is", SI,"rs")

        print("The total amount you will have in", time,"years is", pr+SI,"rs")

        print()

    elif var==6:

        print("Fill the below details to calculate the Compound Interest amount!")

        pr=int(input("Enter Principal Amount : "))

        rate=int(input("Enter Rate of Interest : "))

        time=int(input("Enter Time (in years) : "))

        CI= (pr*((1+(rate/100))**time)) - pr

        print("The Compound Interest is", CI,"rs")

        print("The total amount you will have in", time,"years is", pr+CI,"rs")

        print()

    elif var==7:

        print("Successfully exited the program")

        break

    else :

        print("Invalid option! Please try again..")

        print()

