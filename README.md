item = []
prices = []
quantity = []
total = 0

list_size = int(input("Enter list item size ... "))

for i in range (0,list_size):
  food = input("Enter Item Name")
  qty = int(input(f"Enter  the Quantity of {food}"))
  price = int(input(f"Enter the Price of {food}:Rs."))
  price = qty*price
  item.append(food)
  quantity.append(qty)
  prices.append(price)
  
for i in range (list_size):
  print ((i+1) , "  =   " , item[i] ,  "  = " , quantity[i] , " = " , prices[i] ,"/-")

for price in prices:
  total = total + price

gst = int(input("Add GST (for no 1/ for yes 2)"))
if gst==1:
  print('final_payment')
elif gst==2:
  gst_rate=int(input("Enter GST rate...%"))
else:
  print("invalid choise")

gst_amt = total*gst_rate/100
final_payment = gst_amt+total


print("-------------------------------------------------")
print("-------------------- WELCOME --------------------")
print("-------------------------------------------------")
print("-------------- Prashant Super Store -------------")
print("-------------------------------------------------")
print("Sr. No    Item       Qty         Price")

for i in range (list_size):
  print ((i+1) , "  =   " , item[i] ,  "  = " , quantity[i] , " = " , prices[i] ,"/-")
print("-------------------------------------------------")
print("-------------------------------------------------")
print(f"Your Total is Rs...{total}/-")
print("--------------------------------------------------")
print(f"Your Final Bill is Rs....{final_payment}/-       ")
print("--------------------------------------------------")
print("NOTE* please check your bill ---------------------")
print("    * Carry Bag will be charged extra ----------- ")
print("    * Free home delivery for order above Rs.1000/-")
print("--------------------------------------------------")
print("------------------Thanks for visiting-------------")
print("--------------------------------------------------")
