# xyz

#include <bits/stdc++.h>
#include<iterator>
#include<unordered_map>
using namespace std;

int main()
{
   unordered_map<int ,int>mp;
    int n,val=0,s;
    cin>>n;
    int a[n];
    for(int i=0;i<n;i++)
    {
      cin>>a[i];
     
    }
    for(int i=0;i<n;i++)
      {
          unordered_map<int,int> ::iterator it=mp.find(a[i]);
         if (it != mp.end())
              {
                   it->second++;
              }
              else {
                    mp.insert(make_pair(a[i],1));  
              }
        }
              for(auto &e:mp)
                  {
                       s=e.second;
                      if(s==2)
                          {  val++;continue;}
                        if(s>2)
                          {
                              s/=2; 
                             val +=s;
                          }
                  }
                  
                
      cout<<val;
          
    return 0;
}
