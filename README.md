# stack-permu
class Solution{
public:
    int isStackPermutation(int N,vector<int> &A,vector<int> &B){
        stack<int>st;
        int i=0;
        int j=0;
        while(i<N)
        {
            st.push(A[i]);
    
       while(!st.empty()  && st.top()==B[j]){
           st.pop();
           j++;
       }
       i++;
        }
       
      if(!st.empty() && j!=N)
      {
          return 0;
      }
      else{
          return 1;
      }
    }
};
