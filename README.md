# Compound-Interest-Calculator

# Put Program 1 Code Here. Do not create any additional code blocks or points may be deducted. 
#CIS-443-01
#Program 1
#9/23/24
#This program takes a balance, interest rate, and time in years to calculate compounded interest for every year

#Calls function using principal, interest_rate, and years.
def compounding_interest_calculator(principal, interest_rate, years):
    current = 1
    #The while loop will continue until it reaches the year the user inputs
    while current <= years:

                #calculates the equation, prints the values, and steps up the current year after
                principal = principal * (1 + interest_rate)
                print(f"Year {current} compounded value is ${principal:.2f}")
                current += 1

#Princable balance input
pbal = input("Enter the principle balance: ")

#Checks principle balance for a float value
try:
    pbal = float(pbal)
    #Interest input
    inrate = input("Enter the interest rate: ")

    #Checks interest for a float value
    try:
        inrate = float(inrate)
        #time in years input
        years = input("Enter the number of years: ")

        #checks years for an integer 
        try:
            years = int(years)

            #calls the defined function
            compounding_interest_calculator(pbal, inrate, years)
            
        except ValueError:
            print(years, "is not valid.")
    
    except ValueError:
            print(inrate, "is not valid.")
        
except ValueError:
    print(pbal, "is not valid.")
