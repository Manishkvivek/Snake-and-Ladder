# Snake-and-Ladder/*package whatever //do not write package name here */

import java.io.*;
import java.util.*;
import java.util.Random;


class GFG {
	public static void main (String[] args) {
		
		Random rand=new Random();
		boolean z=true;
		int[] block = new int[2];
		block[0]=0;
		block[1]=0;
		int chance=0;
		while(z)
		{
		    int player=chance+1;
	        int k=rand.nextInt(6)+1;
	        int j=rand.nextInt(3);
	        if(j==1)
	        {
	            int value=0;
	            if(block[chance]-k>0){
	            value=block[chance]-k;}
	            block[chance]=value;
	        }
	        if(j==2)
	        {
	            System.out.println("player"+player+ "got "+k+" from dice");
	            if(block[chance]+k<100){
	            block[chance]=block[chance]+k;
	            System.out.println("positition of p1 ="+block[0]+"  positition of p2 ="+block[1]);
	            continue;
	            }
	            if(block[chance]+k==100){
	                block[chance]=block[chance]+k;
	                System.out.println("positition of p1 ="+block[0]+"  positition of p2 ="+block[1]);
	                System.out.println("Player "+player+" wins the game");
	                break;
	                
	            }
	        }
	        chance=(chance+1)%2;
	        System.out.println("player"+player+ "got "+k+" from dice");
	        System.out.println("positition of p1 ="+block[0]+"  positition of p2 ="+block[1]);

	        if(block[chance]==100)
	        {
	            System.out.println("Player "+player+" wins the game");
	                break;
	        }
		}
		   
	}
}
