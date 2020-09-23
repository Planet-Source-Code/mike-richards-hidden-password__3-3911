<div align="center">

## Hidden Password


</div>

### Description

This code allows the user to imput a password (within a C++ program) without any text being displayed on-screen (not even *'s)
 
### More Info
 
user imputs the characters in the password

getch() allows for real-time imput w/out having to type enter. useful in games and a variety of other applications

password returns true if password was correctly imput, and false if the password was not

no that i know of


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Mike Richards](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/mike-richards.md)
**Level**          |Intermediate
**User Rating**    |5.0 (10 globes from 2 users)
**Compatibility**  |C\+\+ \(general\), Microsoft Visual C\+\+
**Category**       |[Security](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/security__3-14.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/mike-richards-hidden-password__3-3911/archive/master.zip)

### API Declarations

```
#include <conio.h>
#include <iostream.h>
```


### Source Code

```
#include <iostream.h>
#include <conio.h>
bool passcheck(void) //checks password WITHOUT displaying the characters on-screen
{
	char password[7] = "outlaw"; //[] can be used instead, but it takes more memory, its quicker than counting though
	int plen = 6; //plen must be the number of letters in password
	char let;
	for(int i = 0; i < plen; i++)
	{
		let = getch();
		if(password[i] != let)
			return false;
	}
	return true;
}
//the above code immediately returns false if an incorrect password is imput
//if you want it to only return false at the end of the password, create a seperate bool variable
//to be returned at the end of the program
//instead of a for statement you can use (while x != 13) and hit enter at the end of the password
//(13 is the ascii value of enter)
```

