Original Code:
	- Too many if else condition
        - Not declaired variable
	- Not checking if model record exist so it throw error if you call to object that is null
	- Return on the end of the code even if you can return at the beginning so it won't take long time to read the code conditions
	- Not using Query Builder other function when checking if record is null (whereNull) or nut null (whereNotNull)
	- Unnecessary use of findOrFail function so it throw error if doesn't exist
	- Checking if date is less than or equal without changing datetime to timestamp

Refactor Code (I also put a comment to line of code where I refactored)

	- Remove unnecessary if else condition
        - Declaired undeclaired variables at the beggining of the function so it can be accessible if the variable needs to change value and it won't throw error when you return data
	- Check if data exist before procceed to the condition and if data doens't exist I immidiately return it so it won't take long time to read the code
	- Use some Query Builder function like whereNull and whereNotNull
	- Change some findOrFailed function to find
	- Before comparing dates I convert first datetime to timestamp