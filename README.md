# B.-Hamming-Distance-Sum-cideforces
#include <stdio.h>
#include<bits/stdc++.h>
#define ll long long
using namespace std;
  const  ll N=2e5+5;
int A[N]={0};
int main() {
    int c=0;
    ll t=0;
string s,s2;
cin>>s>>s2;
for(int i=0;i<s2.size();i++){
    c+=s2[i]-'0';
    A[i+1]=c;
}
int y=s2.size()-s.size()+1;
for(int i=0;i<s.size();i++){
        int x=A[y+i]-A[i];
    if(s[i]=='0')t+=x;
    else t+=y-x;
}
cout<<t;
 
    return 0;
}
