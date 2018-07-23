# import java.util.Scanner;
public class InserttionSort {
    public static void main(String []args) {
    	int [] array=createArray();
    	int []arrayAfter=insertionSort(array);
    	for(int i=0;i<arrayAfter.length;i++) {
    		System.out.print(arrayAfter[i]+" ");
    	}
    }
             //数组声明，创建，赋值
    public static int []  createArray() {
    	Scanner input=new Scanner(System.in);
    	try {
    		int length;
    		System.out.print("input the length of array:");
    		length=input.nextInt();
    		                                                            //提示用户输入序列长度
    		int [] list=new int [length];
    		System.out.print("input the numbers of array");
    		for(int i=0;i<length;i++) {
    			list [i]=input.nextInt();
    			                                                       //输入序列
    		}
    		return list;
    	}
    	finally {
    		input.close();
    	}
    }
               //选择排序     
    public static int [] insertionSort(int [] egal) {      
    	for(int i=1;i<egal.length;i++) {
    		int currentElement=egal[i];                 //egal[i]为当前要插入的值
    		int k;
    		for(k=i-1;k>=0&&egal[k]>currentElement;k--) {
    			egal[k+1]=egal[k];                       //将第k+1位的值换给第k+2位
    		}
    		egal[k+1]=currentElement;              //将值插入
    	}
    	return egal;
    }
}
insortionSort
