DICE-TEST-LAB---5--WEEK---11
============================
//  BY REINA OLARTE
// "DICE-TEST"  LAB #5  WEEK 11

import java.util.Scanner;

public class DiceTest 
{
	public static void main( String[]args)	
	{
	Scanner input = new Scanner(System.in);

	String Answer;
	int COMPNumber;
	int DICES;
	int bounces;
	boolean SIGA = true;
		while(SIGA)
		{
		System.out.println("How many dices Do  you Want to use?:");
		
		DICES = input.nextInt();
		
		System.out.println("How many bounces Do you want 2"
				+ " each dice to do?:");
		
		bounces = input.nextInt();
		
		Dice myDice = new Dice();
		
		myDice.Throw(DICES, bounces);
		
		System.out.printf("The computer rolled: %d\n" ,myDice.Value());
		
		System.out.println("Would you like to continue?");
		
		Answer = input.next();
		
		if (Answer.toUpperCase().startsWith("N"))
		{
			SIGA = false;
		}
		}
	}
}
