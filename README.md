# prime-number
Function that determines whether a given number is prime or not.

def prime_num_q():
  try:
    number = int(input("please enter an integer value: "))
    num_list = list(range(2, number))
    
    
    if number == 1 or number == 0:
      print("{} is not a prime number".format(number))
    
    elif number < 0 :
      print("please enter an integer value greater than 0(zero): ")  
      print("Please try again.") 
      prime_num_q()          
    elif number == 2:
      print("2 is a prime number")
      
    elif number > 2 :
      prime_fact= []
      for i in num_list:
        if number % i == 0:
            prime_fact.append(number % i) 
      if len(prime_fact) > 0:
        print("{} is not a prime number".format(number))        
      else:
        print("{} is a prime number".format(number))
          
        
  except ValueError:
    print("please enter an integer value greater than 0(zero): ")
    prime_num_q()
  
