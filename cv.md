# Dana Kurmangali
## Contacts
* E-mail: danaeskazi@gmail.com
* Github: [ekdana](https://github.com/ekdana)
  
## About me
Currently, I am a Computer Science student at Nazarbayev University. I am looking for the job or internship where I can improve my hard skills. 

## Skills
* Adobe Photoshop
* Figma
* Microsoft Office
* C/C++
* HTML/CSS 

## Languages
* Kazakh
* English
* Russian
  
## Education
Nazarbayev University, School of Engineering and Digital Sciences, Computer Science

## Experience
* Member of [UNEPG](https://unisat.kz/) by UNICEF Kazakhstan & KazNU
* Robotics trainer
  
## Code Examples
```
#include <stdio.h>

int main() {
	FILE *infile;
	FILE *outfile;

	infile = fopen("in.txt", "r");
	outfile = fopen("out.txt", "w");

	// asking user to enter an input
	int p;
	printf ("Enter the value of p for encryption\n");
	scanf ("%i", &p);

	//checking the properly opening and creation of files
	if (infile== NULL || outfile== NULL){
		printf("Problem opening file\n");
		return 1;
	} else printf("out.txt has been created successfully.\n");

	//getting characters from given file until its end
	char ch, shift;
	while((ch = fgetc(infile))!= EOF){
		// checking if these characters are alphabetic and upper-case;
		// if not, skip and copy them to the output file.
		if ('A'<= ch && ch<= 'Z'){

			//if input(p) more than the number of alphabet letters,
			//rewrite input(p) by equivalent one to reduce a number of circles.
			if (p > 26){
				p = p % 26;
			}

			//shifting character to the p (input) position
			ch = ch + p;

			//after reaching the end (letter Z), encryption restarts from the beginning (letter A)
			int A = 65;
			if (ch > 90){
				shift = ch % 90;
				ch = shift + A - 1;
			}
		}
		//putting encrypted characters in output file
		fputc( ch, outfile );
	}

	fclose(infile);
	fclose(outfile);

	return 0;
}

```
