# HelpIshaan
//{ Driver Code Starts
#include<bits/stdc++.h>
using namespace std;

// } Driver Code Ends
class Solution {
	public:
	bool prime(int N){
	    
	    for(int i=2;i*i<=N;i++){
	        if(N%i==0){
	            return 0;
	        }
	    }
	    return 1;
	}
		int NthTerm(int N){
		   
		    if(N==1){
	        return 1;
		        
		    }
		    if(N==0){
		        return 2;
		    }
		    if(prime(N)){
		        return 0;
		    }
		    int n1=N+1;
		    while(!prime(n1)){
		          n1++;
		          }
		      
		    
		    int n2=N-1;
		    while(!prime(n2)){
		        n2--;
		    }
		    return min(n1-N,N-n2);
		    
		}
		

};

//{ Driver Code Starts.
int main(){
	int tc;
	cin >> tc;
	while(tc--){
		int N;
		cin >> N;
		Solution obj;
		int ans = obj.NthTerm(N);
		cout << ans << "\n";
	}
	return 0;
}
// } Driver Code Ends
