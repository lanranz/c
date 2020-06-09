### 第一题

```
class sortArr{
	static void sort(int[] arr, boolean isAsc){
		if(isAsc){
			for(int i=0;i<arr.length;i++){
				for(j=0;j<arr.length-i-1;j++){
					if(arr[j]>arr[j+1]){
						int temp=arr[i];
						arr[i]=arr[j];
						arr[j]=temp;
					}
				}
			}
		}else{
				for(int i=0;i<arr.length;i++){
					for(j=0;j<arr.length-i-1;j++){
					if(arr[j]>arr[j+1]){
						int temp=arr[i];
						arr[i]=arr[j];
						arr[j]=temp;
					}
				}
			}
		}
	static void sort(int[] arr) {
    	sort(arr, true);
  	}
	static void printArr(int[] arr) {
    	for (int i = 0; i < arr.length; i++) {
      	System.out.printf("[%d]=%d ", i, arr[i]);
      	if ((i + 1) % 5 == 0) {
        System.out.println();
      }
    }
	public static void main(String[] args) {
		int[] arr = {13, 26, -3, 4, 54, 26, 37, 18, 69, -10};
		sort(arr, false);
		printArr(arr);
		System.out.println();
		sort(arr);
		printArr(arr);
	}
}
```

### 第四题

```
class multiply{
	int multiply (int n1,int n2){
    		return n2 != 0 ? n1/(1.0/n2):0;
		}
	public static void main(String[] args) {
	}
}
```

### 第五题

```
public class convert {
  static void convert(long minute) {
    long years = minute / (60 * 24 * 365);
    int days = (int) (minute / 60 / 24) % 365;
    System.out.printf("%d分钟是%d年%d天\n", minute, years, days);
  }
  public static void main(String[] args) {
  }
}
```

### 第六题

```
class CountMoney {

    public static void main(String[] args) {
        int one = 0, two = 0, five = 0, count = 0;
        for (one = 1; one < 150 ; one ++ ) {
            for (two = 1; two < 150 / 2; two++) {
                for (five = 1; five < 150 / 5 ; five++ ) {
                    if (one + two + five == 100 && one + two * 2 + five * 5 == 150) {
                        count++;
                        System.out.printf("%d,%d,%d\n", one, two, five);
                        break;
                    }
                }
            }
        }
        System.out.println(count);
    }
}
```

### 第七题

```
class ArrayFilter {
    public static void main(String[] args) {
        filtArray(new int[] {1, 3, 3, 1, -3, -9, 12, 33});

    }

    static int[] filtArray(int[] target) {
        int finalCount = target.length;
        for (int i = 0; i < finalCount; i++) {
            for (int j = i + 1; j < finalCount ; j++) {
                if (target[i] == target[j]) {
                    target[j] = target[finalCount - 1];
                    finalCount--;
                    j--;
                }
            }
        }

        for (int one : target) {
            System.out.printf("%d ", one);
        }

        System.out.println();

        int[] rlt = new int[finalCount];
        for (int i = 0; i < finalCount ; i++ ) {
            rlt[i] = target[i];
        }

        for (int one : rlt) {
            System.out.printf("%d ", one);
        }
        System.out.println();
        return rlt;
    }
}


```

