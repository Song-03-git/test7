# test7

// [C++] 섭씨(℃) <-> 화씨(℉) 온도 상호 변환기

#include <iostream> // 표준 입출력 스트림(std::cout, std::cin) 헤더 포함

using namespace std; // std 이름공간을 기본으로 사용 설정

int main() {
    int choice; // 메뉴 선택 번호 저장
    double temp; // 입력받을 온도 값 저장

    cout << "1. 섭씨 -> 화씨 변환" << endl;
    cout << "2. 화씨 -> 섭씨 변환" << endl;
    cout << "선택할 메뉴 번호 입력: ";
    cin >> choice;

    if (choice == 1) {
        cout << "섭씨(℃) 온도 입력: ";
        cin >> temp;
        // 섭씨를 화씨로 변환 공식: (℃ * 9/5) + 32
        double fahrenheit = (temp * 9.0 / 5.0) + 32.0;
        cout << "화씨(℉) 온도: " << fahrenheit << "℉" << endl;
    } 
    else if (choice == 2) {
        cout << "화씨(℉) 온도 입력: ";
        cin >> temp;
        // 화씨를 섭씨로 변환 공식: (℉ - 32) * 5/9
        double celsius = (temp - 32.0) * 5.0 / 9.0;
        cout << "섭씨(℃) 온도: " << celsius << "℃" << endl;
    } 
    else {
        cout << "올바르지 않은 메뉴 번호입니다." << endl;
    }

    return 0; // 프로그램 종료
}
