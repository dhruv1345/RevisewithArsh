Link: https://leetcode.com/problems/minimize-the-maximum-of-two-arrays/

code: 

class Solution {
public:
    int minimizeSet(int divisor1, int divisor2, int uniqueCnt1, int uniqueCnt2) {
        int start = 1, end = INT_MAX;
        int ans = INT_MAX;
        long long int lcm = ((long long) divisor1*divisor2)/__gcd(divisor1,divisor2);
        while(start<=end){
            int mid = start + (end - start)/2;
            int notd1 = mid - mid/divisor1;
            int notd2 = mid - mid/divisor2;
            int notboth = mid - mid/lcm;
            if(notd1>=uniqueCnt1 && notd2>=uniqueCnt2 && notboth>=(uniqueCnt1+uniqueCnt2)){
                ans = mid;
                end = mid-1;
            }
            else start = mid+1;
        }
        return ans;
    }

};
