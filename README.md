# Largest-consecutive-sequence
class Solution {
    public int longestConsecutive(int[] nums) {
        
        HashSet<Integer> st = new HashSet<>();
        for (int num : nums) st.add(num);
        int maxStreak = 0;
        for (int num : st) {
            if (!st.contains(num - 1)) { // num is the starting pt of sequence
                int currNum = num; // 1
                int currStreak = 1;  // length of current consecutive sequence
                while (st.contains(currNum + 1)) {
                    currStreak++;
                    currNum++; // 1->2->3.....etc
                }
                maxStreak = Math.max(maxStreak, currStreak);

            }
            }
            return maxStreak;
        }
    }



        
    
