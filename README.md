Write a program to read a string and count the number of vowels using a separate function. 
#include <stdio.h>
int countVowels(char str[]) { int i=0,count=0;

while(str[i]!='\0')
{
    if(str[i]=='a'||str[i]=='e'||str[i]=='i'||str[i]=='o'||str[i]=='u'||
       str[i]=='A'||str[i]=='E'||str[i]=='I'||str[i]=='O'||str[i]=='U')
    {
        count++;
    }
    i++;
}

return count;
}

int main() { char str[100];

printf("Enter a string: ");
fgets(str,sizeof(str),stdin);

printf("Number of vowels: %d",countVowels(str));

return 0;
} output; Enter a string: Hello World Number of vowels: 3
2. Write a function to reverse a string without using library functions like strrev(). 
#include <stdio.h>

void reverse(char str[]) { int len=0,i; char temp;

while(str[len]!='\0')
    len++;

len--;

for(i=0;i<len/2;i++)
{
    temp=str[i];
    str[i]=str[len-i-1];
    str[len-i-1]=temp;
}
}

int main() { char str[100];

printf("Enter string: ");
fgets(str,sizeof(str),stdin);

reverse(str);

printf("Reversed string: %s",str);

return 0;
} output Enter string: Programming Reversed string: gnimmargorP 
3. Write a program to check whether a given string is palindrome or not using functions. #include <stdio.h>

int palindrome(char str[]) { int len=0,i;

while(str[len]!='\0')
    len++;

len--;

for(i=0;i<len/2;i++)
{
    if(str[i]!=str[len-i-1])
        return 0;
}

return 1;
}

int main() { char str[100];

printf("Enter string: ");
scanf("%s",str);

if(palindrome(str))
    printf("Palindrome");
else
    printf("Not Palindrome");

return 0;
} output; Enter string: madam Palindrome 
4. Write a function to calculate the length of a string manually. #include <stdio.h>

int length(char str[]) { int i=0;

while(str[i]!='\0')
    i++;

return i;
}

int main() { char str[100];

printf("Enter string: ");
scanf("%s",str);

printf("Length of string: %d",length(str));

return 0;
} output; Enter string: Computer Length of string: 8 
5. Write a function to count the number of words in a sentence. #include <stdio.h>

int countWords(char str[]) { int i=0,count=1;

while(str[i]!='\0')
{
    if(str[i]==' ' && str[i+1]!=' ')
        count++;

    i++;
}

return count;
}

int main() { char str[100];

printf("Enter sentence: ");
fgets(str,sizeof(str),stdin);

printf("Number of words: %d",countWords(str));

return 0;
} 
output; Enter sentence: C programming is easy Number of words: 4
