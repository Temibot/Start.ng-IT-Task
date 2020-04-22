from random import choice
from string import ascii_letters

def user_signup(): 
	userFirst = input("Enter your first name: ")
	userLast = input("Enter your last name: ")
	userMail = input("Enter your email address: ")
	userDict = {"firstname": userFirst, "Last name": userLast, "Email": userMail}

	return userDict

userlist = []


def generate_password():
	user_sign=user_signup() #I called this function here
	user_password = user_sign["firstname"][0:2] + user_sign["Last name"][-2:] + "".join(choice(ascii_letters)for i in range(6)) # i changed userDict to usersign since i have called the return value of user_signup as suer_sign

	print(f"Do you like this password to be used for your  profile: {user_password} , yes/no")
	passAnswer = input("Enter 1 if yes, if not enter 0: ")
	while True:
		if passAnswer == '1': 
			user_sign["password"] = user_password #I added password into dictionary if the user wants it. I also changed the dictionary name due to the result i called from function1
			break
		elif passAnswer == '0':

			newPassword = input("Type your preferred password. Your password has to be greater than 7 characters: ")
			if len(newPassword)>=7:
				user_sign["password"] = newPassword
				break
			else:
				newPassword

		
		else:
			passAnswer = input("Enter 1 if yes, if not enter 0: ")#added a while loop incase user doesnt type 0 or 1

	userlist.append(user_sign)

	startStop() #after finishing loop1, i jump back to loop 2

def startStop():
	user_remain = input("Are you a new employee?: Enter 1 if yes, if not enter 0 ")
	while True:
		if user_remain == '1':
			return generate_password()
		elif user_remain == '0':
			for user in userlist:
				print(f"Welcome {user['firstname']} {user['Last name']}. Your email address is {user['Email']} and your password is {user['password']}")
			break
		else:
			startStop()
startStop()
