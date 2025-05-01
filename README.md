# Cricket-Team-Score-Analyzer
A simple Java console application that takes the scores of players from two cricket teams, calculates the total team scores, determines the winning team, and identifies the highest individual scorer as the "Man of the Match." This project demonstrates basic array handling, user input with Scanner, and control structures in Java.

code:
package org.demo;

import java.util.Scanner;

public class classtest {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
int teamA=0,teamB=0,maxrun=0;
String win="";
int[] arrA=new int[11];
int[] arrB=new int[11];
Scanner sc=new Scanner(System.in);
System.out.println("enter the score of the player on team A");
for(int i=0;i<11;i++) {
	arrA[i]=sc.nextInt();	
}
System.out.println("enter the score of the player on team B");
for(int j=0;j<11;j++) {
	arrB[j]=sc.nextInt();
}
for(int i=0;i<11;i++) {
	teamA=teamA+arrA[i];
	if(maxrun<arrA[i]) {
		maxrun=arrA[i];
	}
}
for(int j=0;j<11;j++) {
	teamB=teamB+arrB[j];
	if(maxrun<arrB[j]) {
		maxrun=arrB[j];
	}
	}
	if(teamA>teamB) {
		win="Team A";
	}
	else {
		win="Team B";
	}

System.out.println("winning team is "+win);
System.out.println("total score by team A is"+ " "+teamA+" " +"total score by team B is"+" "+ teamB);
System.out.println("man of the match runs are "+ maxrun);
	}
}

