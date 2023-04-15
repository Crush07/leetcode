```java
class Solution {
    public boolean isPalindrome(int x) {
        if(x < 0){
            return false;
        }else if(x >= 0 && x < 9){
            return true;
        }else{
            StringBuilder sb = new StringBuilder(Integer.toString(x));
            if(sb.toString().equals(sb.reverse().toString())){
                return true;
            }else{
                return false;
            }
        }
    }
}
```

1. 如果是负数则一定不是回文数，因为没有一个完整的数字会在末尾出现符号
2. 如果是个位数这一定是回文数
3. 如果上面多位数这把x转换成`StringBuilder`利用其可以翻转字符串的api，和原字符串对比是否一致

