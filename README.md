Пурясьев выполнил
# readmeLab1Puryasev
#include <iostream>
#include <cmath>


using namespace std;

bool isInteger(float num) {
    return fmod(num, 1.0) == 0.0;
}

int main() {
    int a, b, c;
    cin >> a >> b >> c;
    if (c < 0) {
        cout << "NO SOLUTION" << endl;
        return 0;
    }
    if (a == 0) {
        if (sqrt(b) != c) {
            cout << "NO SOLUTION" << endl;
            return 0;
        }
        cout << "MANY SOLUTIONS" << endl;
        return 0;
    }

    float result = (c * c - b) / (float)a;

    if (!isInteger(result)) {
        cout << "NO SOLUTION";
        return 0;
    }

    cout << result << endl;
    system("pause");
    return 0;
}
