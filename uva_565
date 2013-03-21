/*
 Author                             :     unlucky_13
 Probs_link                         :     http://uva.onlinejudge.org/index.php?option=onlinejudge&page=show_problem&problem=565
 Algorithm_Used                     :     DP-knaspsack

*/

#include<cstdio>
#include<sstream>
#include<cstdlib>
#include<cctype>
#include<cmath>
#include<algorithm>
#include<set>
#include<queue>
#include<stack>
#include<list>
#include<iostream>
#include<fstream>
#include<numeric>
#include<string>
#include<vector>
#include<cstring>
#include<map>
#include<iterator>
#define LL long long int
//const int MIN =
const int MAX = 10000 ;
int dp[21][MAX] ;
int track[MAX] ;
int play[21] ;
using namespace std;
void playlist(int T){

  if(T==0) return ;

	playlist(T-play[track[T]]) ;
    cout<<play[track[T]]<<" ";

}
int main() {
  freopen("C:\\Users\\Mazhar\\Desktop\\in.txt","r",stdin) ;

  int t,n ;



  while(scanf("%d %d",&t,&n)==2){

	  for(int i=1;i<=n;i++)
		  scanf("%d",&play[i]) ;


	  for(int i=1;i<=n;i++){
		  for(int j=1;j<play[i];j++)  dp[i][j] = dp[i-1][j] ;
		  for(int j=play[i];j<=t;j++){
			 // cout<<dp[i-1][j]<<" "<<dp[i-1][j-play[i]]+play[i]<<endl ;
			  if(dp[i-1][j]>=dp[i-1][j-play[i]]+play[i]) dp[i][j] = dp[i-1][j] ;
			  else{
				  dp[i][j] = dp[i-1][j-play[i]]+play[i] ;
				  track[dp[i][j]] = i ;

			  }
		  }

	  }

       //for(int i=0;i<=dp[n][t];i++) cout<<track[i]<<" " ;
      playlist(dp[n][t]) ;
      printf("sum:%d\n",dp[n][t]) ;


  }






  return 0;
}
