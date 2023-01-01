#include <iostream>
#include <vector>

using namespace std;


long getCardCount(int n, int k, const vector<long long> &cards) {
    int sum = 0;
    int temp = 0;
    int rightIndex = cards.size() - 1;
    for (int i = 0; i < k; ++i) {
        sum += cards[i];
    }
    temp = sum;
	if (n > k) {
        for (int i = k - 1; i >= 0; --i) {
            temp = temp - cards[i] + cards[rightIndex];
            if (temp > sum) {
                sum = temp;
            }
            --rightIndex;
        }
    }
    return sum;
}

int readInt() {
    int x;
    cin >> x;
    return x;
}

vector<long long> readList(int n) {
    vector<long long> res(n);
    for (int i = 0; i < n; i++) {
        cin >> res[i];
    }
    return res;
}

int main() {
    int n = readInt();
    int k = readInt();
    vector<long long> cards = readList(n);
    cout << getCardCount(n, k, cards);
}
