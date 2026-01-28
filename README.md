# Expense-tracker
An expense tracker where you can add expenses to the current expense list, view the expenses currently added, and add all the expenses currently in the expense list or exit the program 

expense_ = []

def add_expense(expense_):
	try:
		amount = float(input('enter an expense amount: '))
		if amount > 0:
			expense_.append(amount)
		else:
			print('amount must be positive!')
	except ValueError:
		print('invalid number!')
	
def view_(expense_):
	print('expense: ')
	for expense in expense_:
		print(expense)


def total_spent(expense_):
		return sum(expense_)


def greet(name):
	print('Hello!', name)

name = input('Enter your name: ')
greet(name)
# menu
while True:
	print('\n 1. Add expense')
	print('2. view expense')
	print('3. view total spent')
	print('4. exit')
	
	option = input('choose an option: ')
	if option == '1':
		add_expense(expense_)

	elif option == '2':
		view_(expense_)

		
	elif option == '3':
		print('sum:', total_spent(expense_))
	

	
	elif option == '4':
		print('Goodbye!')
		break
	else:
		print('Invalid option, try again!')
