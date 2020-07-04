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
		
	
		
				
		
#building a Body Mass Index calculator
#input the parameters with the name of the person and enjoy.....


name = input('name:')
height_m = int(input('height:'))
weight_kg = int(input('weight:'))

bmi = weight_kg/(height_m**2)
print("bmi:")
print(bmi)
if bmi < 20:
		print(name)
		print("is not overweight and healthy ")
else:
		print(name)
		print("is overweight and unhealthy	")
		

		
						
		#speed calculator
#calculate the speed by inputting the name of the car and the following parameters and its applicable to the other calculators.....


name = input("enter the name of the vehicle to calculate the speed: ") 
distance_km =  float(input("distance:"))
time_h =   float(input("time: "))

speed = (distance_km/ time_h)
print(speed)
if speed < 100:
	print(name + " has not exceed speed limit")
else:
	print(name + " has exceed speed limit")
	
	
#time calculator
name =  input("enter the name of the vehicle to calculate the time: ")
distance_km =float(input("distance:"))
speed_km =  float(input("speed: "))

def time_calculator(name, distance_km, 		speed_km):
	time = (distance_km/speed_km)
	print(time)
	if time < 1:
		return name + " arrived very slow"
	else:
		return name +  " arrived very accurate"
result = time_calculator (name, distance_km, speed_km)
print(result)


#distance calculator
name =  input("enter the name of the vehicle to calculate the distance: ")
speed_km =  float(input("speed: "))
time_h =  float(input("time: "))
distance = (speed_km * time_h)
print(distance)
if distance <1000:
	print(name + " covers an average distance")
else:
	print(name + " covers an accurate distance ")
