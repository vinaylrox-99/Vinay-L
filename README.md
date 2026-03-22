class vi:
 def __init__(self,phone_number,balance):
    self.__phone_number=phone_number
    self.__balance=balance
    self.menu()
 def menu(self):
  while True:
    print('''
    1) press 1 for add_balance
    2) press 2 for check balance
    3) press 3 for add data pack
    4) press 4 for make_call
    5) press 5 for exit''')

    try:
        choice = int(input('enter the choice'))
    except ValueError:
        print("Invalid input. Please enter a number between 1 and 5.")
        continue

    if choice == 1:
      self.add_balance()
    elif choice == 2:
      self.check_balance()
    elif choice == 3:
      self.add_datapack()
    elif choice == 4:
      self.make_call()
    elif choice == 5:
      print("Thank you ")
      break
    else :
      print('Invalid choice. Please select from 1-5.')

 def add_balance(self):
    print('''
    1) press 1 for 349 recharge
    2) press 2 for 379 recharge
    3) press 3 for 399 recharge''')

    choice2 = input('enter the choice')
    if choice2 =="1":
      print('you have choosed the 349 recharge')
      amount = int(input('enter the amount'))
      if amount == 349:
        self.__balance = self.__balance + amount
        print('recharge successful')
        print('Now you can enjoy with 2GB/day and ut call and 100 msg/day',self.__balance)

      else:
        print('Enter correct amount')

    elif choice2 =="2":
         print('you have choosed the 379 recharge')
         amount = int(input('enter the amount'))
         if amount == 379:
          self.__balance = self.__balance+amount
          print('recharge successful')
          print('Now you can enjoy with 2GB/day and ut call and 100 msg/day and ul for 5G',self.__balance)

         else:
          print('Enter correct amount')

    elif choice2 =="3":
         print('you have choosed the 399 recharge')
         amount = int(input('enter the amount'))
         if amount == 399:
          self.__balance = self.__balance+amount
          print('recharge successful')
          print('Now you can enjoy with 2GB/day and ut call and 100 msg/day and ul for 5G and 1 month jio hotster',self.__balance)

         else:
          print('Enter correct amount')
    else :
      print('Enter valid choice')

 def check_balance(self):
    print("Your balance is : ",self.__balance)

 def add_datapack(self):
    print('''
    1) press 1 for 2GB data for 40rs
    2) press 2 for 1.5GB data for 30rs
    3) press 3 for 1GB data for 20rs ''')

    choice3=input('enter your choice')
    if choice3 == '1':
      print('You have choosed the 2GB pack')
      amount2 = int(input('Enter the amount'))
      if amount2 == 40:
        print('You have recharged 2GB data for only till mid night 12:00 Am')

      else :
        print('Enter valid amount')

    elif choice3 == '2':
      print('You have choosed the 1.5GB pack')
      amount2 = int(input('Enter the amount'))

      if amount2 == 30:
        print('You have recharged 1.5GB data for only till mid night 12:00 Am')

      else :
        print('Enter valid amount')

    elif choice3 == '3':
      print('You have choosed the 1GB pack')
      amount2 = int(input('Enter the amount'))
      if amount2 == 20:
        print('You have recharged 1GB data for only till mid night 12:00 Am')
        self.d["recharge 20"]=[amount2]
      else :
        print('Enter valid amount')
    else :
      print('Enter valid choice')

 def make_call(self):
    minutes=int(input('Enter the minutes'))
    cost=minutes*2
    if cost <=self.__balance:
      self.__balance = self.__balance - cost
      print("Call successful, you can connect now!")
      print("Your remaining balance is",self.__balance)
      print("Cost of call is:",cost)

    else:
      print("Please recharge yourself")
      self.add_balance()
user = vi('9584395800', 0)
