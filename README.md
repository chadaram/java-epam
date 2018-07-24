# java-epam
# largest palindrome product of two  n digit numbers
package javaq;
import java.io.*;
import java.util.*;

public class A {
public static void main(String args[])
{
	int c,d,m=0,a,f=1,g=1;
Scanner s=new Scanner(System.in);
a=s.nextInt();
while(a>0)
{
g*=10;
a-=1;
}
A b=new A();
for (int i=g-1;i>g%10-1;i--)
{
	for(int j=g-1;j>g%10-1;j--)
	{
		c=j*i;
		d=b.pal(c);
		if (d>m)
		{
			m=d;
		}
	}
}
System.out.println(m);
}

int pal(int c)
{
	int p,k=0,h=c;
	while(h>0)
	{
	p=h%10;
	k=k*10+p;
	h=h/10;
}
if (c==k)
{
return k;
}
else
{
	return 0;
}
}
}

