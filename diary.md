entry 1: develop the spending function 
date : 13/10/2026
what i was trying to do(goal): i wanted to develop a budget calculator for my budgetlow project application that could calculate monthly expenses and shows users their balance remaining after spending.
my approach: i worked on the code by myself by went back to have a look at my lab ticket for module 6, but my code was wrong because got stuck and confuse on how to use calculate the total using sum() and remaining 
balance. this is my prompt for asking ai "Can you help me make the output show money with two decimal places and explain what changes I need to make? Please keep my original code structure simple because I'm still learning Python.

def calculate_budget(income, expenses):
total_expenses = sum(expenses)
remaining_balance = income - total_expenses

return total_expenses, remaining_balance

monthly_income = 3500
monthly_expenses = [600, 350, 400, 800]

total, remaining = calculate_budget(monthly_income, monthly_expenses)

print("Total expenses: $", total)
print("Remaining balance: $", remaining)" gemini response with a longer cells which makes me decided not to use that because it makes me more confusing.
reflection: this part help me to understand hwo python function can accept values , do the calculation and shows the result. i learned that even the function works correcty , its output can still be improved to make the application more easiler for users.
