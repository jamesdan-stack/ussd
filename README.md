# ussd


#designing an ussd command

print("Welcome to Glo")
restart = ('y')
balance = 567.36
data = 671

while restart not in ('n', 'no', 'NO', 'N'):
	
#this are the commands meant to be selected to access the USSD service

	print("\nPlease press 1 for balance\n")
	print('Please press 2 for data balance\n')
	print('Please press 3 for recharge from your conneted bank account\n')
	print('Please press 4 to exit\n')

	option = int(input('what would you like to choose? '))
	
	if option == 1:
		print('\nYour account balance is',balance,)
		restart = input('would you like to go back?')
		if restart in ('n','no','NO','N'):
			print('Thank you!')
			break
			
	elif option == 2:
		print('\nYour data balance is', data,'mb',)
		restart = input('would you like to go back?')
		if restart in ('n','no','NO','N'):
			print('Thank you!')
			break
			
	elif option == 3:
		buy = float(input('How much would you like to recharge?'))
		balance = balance + buy
		print('\nYour recharged balance is now', balance, )
		restart = input('Would you like to go back?')
		if restart in ('no', 'n', 'NO', 'N'):
				print('Thank you!')
				break
				
	elif option == 4:
		print('\nThank you for choosing GLO.')	
		break
