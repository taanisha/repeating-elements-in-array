#include <bits/stdc++.h>

using namespace std;

int main()
{
    int arr[]= { 2, 0, 2, 1, 4, 3, 1, 0 };
    int l=sizeof(arr)/sizeof(arr[0]);
    pair<int,int>p;
    vector<pair<int,int>>ans;
    for(int i=0;i<l;++i){
        for(int j=i+1;j<l;++j){
            if(arr[i]==arr[j]){
                ans.push_back(make_pair(i,j));
            }
        }
    }
    int c=0;
   
   int s,e;
    for(int i=0;i<ans.size();++i){
        if(c<ans[i].second-ans[i].first){
            c=ans[i].second-ans[i].first;
            s=ans[i].first;
            e=ans[i].second;
        }
    }
    for(int i=s;i<e;++i){
        cout<<arr[i]<<" ";
    }
    return 0;
}

