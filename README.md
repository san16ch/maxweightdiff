# maxweightdiff

import java.util.Arrays;
import java.util.Iterator;
import java.util.Scanner;
public class Max_weight
{

	public static void main(String[] args)
	{
		// TODO Auto-generated method stub
		Scanner sc= new Scanner(System.in);
		System.out.println("enter no of items bought");
		int N=sc.nextInt();
		System.out.println("enter no of items in one group");
		int K=sc.nextInt();
		System.out.println("enter weight of" +N+"items");
		int a[]=new int[N];
		for(int i=0;i<N;i++) {
			a[i]=sc.nextInt();
		}
		Arrays.sort(a);
		int p1weight=0;
		int p2weight=0;
		for(int l=0;l<K;l++) {
			p1weight=+a[l];
		}
		for(int z=N-K-1;z<=N-1;z++) {
			
			p2weight=+a[z];
		}
	 int maxwtdiff=0;
	 maxwtdiff=Math.max(p1weight, p2weight) - Math.min(p2weight, p1weight);
		System.out.println(maxwtdiff);
	}

}
