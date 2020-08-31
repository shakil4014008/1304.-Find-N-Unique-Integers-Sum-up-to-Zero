# 1304.-Find-N-Unique-Integers-Sum-up-to-Zero

 

```C#
 public class Solution {
    public int[] SumZero(int n) {
        if(n == 1)  return new int[1]{0};
        
        List<int> list = new List<int>();
        int count = 0;
        int [] arrRight = new int[count];
        int [] arrLeft = new int[count];
        
        if(n % 2 == 0){
            count = n/2;
            for(int i=1; i<=count; i++){
                list.Add(i);
            }
            for(int i=1; i<=count; i++){
                list.Add((-1)*i);
            }
            
        }else{
            list.Add(0);
             count = n/2;
            for(int i=1; i<=count; i++){
                list.Add(i);
            }
            for(int i=1; i<=count; i++){
                list.Add((-1)*i);
            }
        }
        
        return list.ToArray();
    }
    
}
```

## Complexity Analysis
 
