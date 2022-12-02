# LEETCODE-PRACTICE

#include <bits/stdc++.h>
using namespace std;
void solve(vector<int>& arr)
{
    int low = 0;
    int mid = 0;
    while(mid < arr.size())
    {
        if(arr[mid] & 1 == 1)
        {
            mid++;
        }else{
            swap(arr[mid], arr[low]);
            mid++;
            low++;
        }
    }
}

int main()
{
    int n;
    cin >> n;
    vector<int> arr;
    for(int i = 0; i < n; ++i)
    {
        int k;
        cin >> k;
        arr.push_back(k);
    }

    for(int i = 0; i < n; ++i)
    {
        cout << arr[i] << " ";
    }

    cout << endl;

    solve(arr);

    for(int i = 0; i < n; ++i)
    {
        cout << arr[i] << " ";
    }

    cout << endl;
}
