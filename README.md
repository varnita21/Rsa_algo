# Rsa_algo
Rsa algorithm in cryptography network security 
#include<stdio.h>
#include<conio.h>
#include<string.h>
#include<math.h>

int fgcd(int n,int l);

void main() {
	clrscr();
	int e,p,q,n,l,i,j,gcd,ln;
	char text[20];
	char cipher[20];
	printf("Enter the text\t");
	scanf("%s",&text);
	ln= strlen(text);
	printf("Enter the two prime numbers p and q:\t");
	scanf("%d %d",&p,&q);

	n=p*q;
	l=(p-1)*(q-1);
	e = fgcd(n,l);
	for(i=0;i<ln;i++){
		int m = text[i];
		cipher[i] = (m^e)%n;
		printf("%d",cipher[i]);
	}
	printf("The cipher text:\t");
	for(i=0;i<ln;i++) {
		printf("%c",cipher[i]);
	}
	for(i=0;i<ln;i++) {
		int v = (cipher[i]^)

	getch();

}
int fgcd(int n,int l){
	int g,i;
	for(i=1;i<=n && i<=l;i++){
		if(n%i==0 && l%i==0)
			g = i;
	}
	return g;
}