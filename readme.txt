public class InsertionSort {
	public static void insertionSort(int[] array){
		if(array==null||array.length<2){
			return ;
		}
		for(int i = 0;i<array.length;i++){
			int currentValue = array[i];
			int position = i;
			for(int j = i-1;j>=0;j--){
				if(array[j]>currentValue){
					array[j +1] = array[j];
					position -=1;
				}else{
					break;
				}
			}
			array[position] = currentValue;
		}
	}
	
	
	public static void main(String[] args){
		int [] array = {3,10,5,2,14,9,8};
		ArrayUtils.printArray(array);
		insertionSort(array);
		System.out.println();
		ArrayUtils.printArray(array);
	}
}


class ArrayUtils{
	public static void printArray(int[] array){
		System.out.print("{");
		for(int i = 0;i<array.length;i++){
			System.out.print(array[i]+",");
		}
		System.out.print("}");
	}
}