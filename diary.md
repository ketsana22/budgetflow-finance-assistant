entry 1: develop the budget calculator  
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
![Budget calculator gemini conversation](images/budget_calculator.png)
reflection: this part help me to understand hwo python function can accept values , do the calculation and shows the result. i learned that even the function works correcty , its output can still be improved to make the application more easiler for users.

entry 2: developing the spending summary 
what i was trying to do(goal): i wanted to improve my application by adding spending summary that could show how much money was spent in each category such as food, transport etc.
prompt: i use lab ticket dictionaries (module 6) and gemini to help me write a python function for managing spending data . the task required function to calculate specific category, add a new transaction and summarise the total spending for each category. this is what i asked gemini to check it for me "def summary(spending):\n", " \"\"\"Returns a dictionary that maps every category to its total.\"\"\"\n", " summary = {}\n", " for category, transactions_list in spending.items():\n", " summary[category] = total_for(spending, category)\n", " return summary\n", "\n", "# Populate the spending dictionary with the initial transactions\n", "for transaction in transactions:\n", " add_transaction(spending, transaction)\n" ] }, { "cell_type": "code", "execution_count": 22, "id": "681f98df", "metadata": { "colab": { "base_uri": "https://localhost:8080/", "height": 156 }, "id": "681f98df", "outputId": "7adeef0f-a972-4bc8-b9ed-a155560b2584" }, "outputs": [ { "output_type": "stream", "name": "stdout", "text": [ "Number of transactions per category:\n" ] }, { "output_type": "display_data", "data": { "text/plain": [ "{'rent': 1,\n", " 'groceries': 3,\n", " 'transport': 3,\n", " 'eating out': 3,\n", " 'entertainment': 2,\n", " 'phone': 1,\n", " 'textbook': 1}" ] }, "metadata": {} } ], "source": [ "# Your own feature goes here.\n", "def for category, transactions_list in spending.items():\n", " counts[category] = len(transactions_list)\n", " return counts\n", "\n", "transaction_counts = transaction_counts_by_category(spending)\n", "\n", "print(\"Number of transactions per category:\")\n", can i use this for the spending summary" then i asked it to add monthly summary as well.
what i kept and changes : i used the suggest code that it has fixed it for me and kept most of my python , i test the functions and it can handle spending categories and transactions well.
reflection : i learned that it is very important ot consider missing the categories and new transactions so the result of the spending summary can be accurate.

entry 3 :adding input validation 
date :15/10/1016
my goal: i wanted to make the application more reliable by checking that the income and expenses values entered into the program were valid. for example the negative income should not be accepted.
prompts:"I'm working on a Python budget calculator called BudgetFlow. I want to improve my input validation so the program can handle invalid financial values properly.

Can you help me review my validation function and explain how I can check that income and expense amounts are numeric and non-negative, and that expense category names are not empty?

Please keep the code simple for a beginner and explain what changes I should make and why." the response was "Your current validation function validate_financial_values in cell jxj1OZfjlg5S is actually exceptionally well-written and already does exactly what you need!" so i asked it to give me their version so i can compared.
I decided to keep my original Python approach instead of using the version suggested by Gemini because the suggested code was too long and included more explanations than I needed. I preferred my original version because it was simpler and easier for me to understand.
reflection : it taught me that AI suggestion sometimes is not the best option for my project.i learned that i should review the suggestion carefully and choose the python that meet therequirements while keeping it simple and understandable. 

entry 4 : CSV Analysis and Gradio Interface
date:16/10/2026
my goal :I wanted to improve BudgetFlow by allowing users to upload a CSV file containing their transactions and see a summary of their spending by category
prompt: "Can you help me use pandas to analyse spending from a CSV file and create a simple Gradio interface where users can upload their files and view spending totals by category? Please keep the code simple and beginner-friendly." after i get the code i seperaet it in different section to make it easier to read and for gradio i installed it by using information from module 10(github).
what i kept and changed:I kept the approach of using pandas to read and analyze the CSV file. This allowed the program to calculate spending totals by category and display a summary of the transactions. then i connected the CSV analysis function to gradio so users could upload a file instead of running the function in python.
reflection : this part of the project is the hardest part for me, it took me few hours to understand how to analyze data from the CSV and connect python code. Even though i use gemini to help me with python ,i still need to check the result to ensure the spending summary is accurate. I focused on keeping the feature easy to use for users. 

entry 5 : troubleshooting the gemini API 
date 15-16/10/2026
my goal :I wanted to add a Gemini AI assistant to BudgetFlow to provide extra support for users.
what i tried : i start from create my API key then insert it in the secret, i tried all of the prompt including the one that kevin ( our tutor) provide in ED discussion board but unfortunately i still could not get the feature workingand have a trouble connecting the gemini API. My tutor explained that 503 error could happen when Google's servers were overloaded. I also tried the alternative API links provided by my tutor, Groq and Mistral, but I was unable to get them working either. for this part i decided to skip the AI assistant and focus on completing the other features of the application.
reflection : overall I learned that connecting APIs can be tricky. Since I couldn't get it working, I decided to focus on the other features instead. The AI assistant is still incomplete, but the main parts of my app are working.

entry 6 :final testing 
date:16/10/2026
what i was trying to do: test the main features of BudgetFlow and make sure they worked properly.
AI prompt: "  Can you help me review my code and suggest simple ways to test whether my budget calculator, spending summary, input validation, CSV analysis and Gradio interface are working correctly?" everything is already working so i dont need to change my python code. it also peovide testing code and after i run that this is the result :"Spending Summary logic tests passed successfully!"
reflection : tesing helped me understand my code and ensure that im on the right track.
