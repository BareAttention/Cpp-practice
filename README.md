# Cpp-practice
#include <iostream>
using namespace std;
#include <vector>
#include <algorithm>
#include <numeric>
#include <cstdlib>

int main()
{
    int n, m, i, j, t, c;
    cin >> n >> m;
    vector <int> cost;
    for (i = 0; i < n; i++) {
        cin >> c;
        cost.push_back(c);
    }
    sort(cost.begin(), cost.end());
    for (j = 0; cost[j] < 0 && j < m; j++);
    int sum = accumulate(cost.begin(), cost.begin() + j, 0);
    cout << abs(sum);
    return 0;
}
