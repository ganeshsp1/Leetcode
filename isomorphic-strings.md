Given two strings s and t, determine if they are isomorphic. (one to one mapping)


ANSWER:

Check the link https://www.educative.io/edpresso/how-to-check-if-two-strings-are-isomorphic for clearer explanation.

```
class Solution {
    public boolean isIsomorphic(String s, String t) {
        HashMap<Character,Character> charMap = new HashMap();
        Set set = new HashSet();
        for(int i = 0; i< s.length();i++){
            Character c = s.charAt(i);
            Character tc = t.charAt(i);
            if(charMap.get(c)!=null){
                if(charMap.get(c)!=tc) return false;
            }else if(set.contains(tc)){
                if(charMap.get(c)!=tc) return false;
            }else{
                charMap.put(c,tc);
                set.add(tc);
            }
        }
        return true;
    }
}

```
