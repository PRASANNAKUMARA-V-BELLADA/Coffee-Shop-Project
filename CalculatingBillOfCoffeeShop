class CoffeeShop:
  def calculateBill(self):
   print("Welcome To Coffee Store")
   print("Please select an item from the menue:")
   print("1.Espresso-Rs 10.00")
   print("2.Cappuccino-Rs 12.50")
   print("3.Latte-Rs 15.00")
   print("4.Mocha-Rs 14.75")
   print("5.Black Coffee-Rs 12.50")
   lst=[]
   app={1:['Espresso',10.00],2:['Cappuccino',12.50],3:['Latte',15.00],4:['Mocha',14.75],5:['Black Coffee',12.50]}
   while True:
       try:
         choice=int(input("Enter Your Choice->"))
       except:
           print("You Entered Text,Please Make Choice In Numbers\n")
           continue
       if choice in app.keys():
           lst.append(choice)
           while True:
               print()
               ask=str(input("Are Your Want To Add Another Item(Yes/No):"))
               if ask.isnumeric():
                 print("You Should Enter Either Yes Or No")
                 continue
               else:
                   break
           
           if ask.lower()=='yes':
               print("Again",end=" ")
               continue
           elif ask.lower()=='no':
               break
       else:
           print("Your Choice Is Not There Please Try Again")
   print()
   print("You Ordered")
   for i in lst:
        data=app.get(i)
        print("{0}-Rs {1:.2f}".format(data[0], data[1]))
   print()
   while True:
    a=input("Are You Want To Remove Any Item from Your Order(yes/no):")
    if a.lower()=='yes':
       while True:
          try:
              b=int(input("Enter The Item Number Of Your Order Items:"))
          except:
               print("Item Number Must Be In Numbers")
               continue
          if b in lst:  
              lst.remove(b)
              break
          else:
            print("Item Number Is Not There In Your Order,Please Try Again")
            continue
       print()
       print("Again",end=" ")
    else:
        break
   print()
   print("You Ordered")
   for i in lst:
        data=app.get(i)
        print("{0}-Rs {1:.2f}".format(data[0], data[1]))
   print()
   total=0
   if len(lst)>1:
        for i in lst:
            data=app.get(i)
            total+=data[1]
   else:
       data=app.get(i)
       total=data[1]
   print("Total Bill(before tax):%.2f" % total)
   tax=(5*total)/100
   total=tax+total
   print("Total Bill(with 5% tax):{:.2f}".format(total))
   if total>50:
       disc=(10*total)/100
       total=total-disc
       print("Your Order is Above 50 So 10% discount")
       print("Now Total Bill Is %.2f" % total)

if __name__=='__main__':
    obj=CoffeeShop()
    obj.calculateBill()
