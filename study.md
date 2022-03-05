// #include <iostream>
// #include <tchar.h>
// using namespace std;


// void TestFunc(const int &nParam)
// {
//     int &nNewParam = const_cast<int &>(nParam);
//     nNewParam = 20;
// }

// int _tmain(int argc, _TCHAR* argv[])
// {
//     int nData = 10;

//     TestFunc(nData);

//     cout << nData << endl;

//     return 0;
// }
// #include <iostream>
// #include <tchar.h>
// using namespace std;

// class CMyData
// {
// public:
//     CMyData() : m_nData(0) { };

//     int GetData(void) {return m_nData;}
//     void SetData(int nParam) { m_nData = nParam;}

//     void SetData(double dParam) { m_nData = 0;}
// private:
//     int m_nData;
// };
// int _tmain(int argc, _TCHAR *argv[])
// {
//     CMyData a;
//     a.SetData(10);
//     cout << a.GetData() << endl;

//     CMyData b;
//     b.SetData(5.5);
//     cout << b.GetData() << endl;
//     return 0;
// }
// #include <iostream>
// #include <tchar.h>
// using namespace std;

// class CMyData
// {
// public:
//     CMyData() : m_nData(0) { };

//     int GetData(void) { return m_nData;}
//     void SetData(int nParam) { m_nData = nParam;}

//     void SetData(double nParam) = delete;

// private:
//     int m_nData;
// };
// int _tmain(int argc, _TCHAR *argv[])
// {
//     CMyData a;
//     a.SetData(10);
//     cout << a.GetData() << endl;

//     CMyData b;
//     b.SetData(5.5);
//     cout << b.GetData() << endl;
//     return 0;
// }
// #include <iostream>
// #include <tchar.h>
// using namespace std;
// class CTest
// {
// public:
//     CTest(int nParam) : m_nData(nParam) { m_nCount++; }
//     int GetData() {return m_nData; };
//     void ResetCount() { m_nCount = 0;}

//     static int GetCount()
//     {
//         return m_nCount;
//     };
// private:
//     int m_nData;
//     static int m_nCount;
// };
// int CTest::m_nCount = 0;

// int _tmain(int argc, _TCHAR *argv[])
// {
//     CTest a(5),b(10);
//     cout << a.GetData() << endl;
//     b.ResetCount();
//     cout << CTest::GetCount() << endl;
//     return 0;
// }
// #include <iostream>
// #include <tchar.h>
// using namespace std;
// class Neuron
// {
//     public:
//     double w_;
//     double b_;
    
//     double GetAct(const double& x)
//     {
//         return x;
//     }

//     double Feedforward(const double& Input)
//     {
//         const double sigma = w_ * Input + b_;
//         GetAct(sigma);
//     }
// };
// int main(void)
// {   
//     Neuron my_neuron;
//     my_neuron.w_ = 2.0;
//     my_neuron.b_ = 1.0;
//     cout << my_neuron.Feedforward(1.0) << endl;
//     return 0;
// }
// #include <iostream>
// #include <tchar.h>
// using namespace std;
// int _tmain(int argc, _TCHAR argv[])
// {
    
//     return 0;
// }
// #include <iostream>
// #include <tchar.h>
// using namespace std;
// class CMyData
// {
// public:
//     CMyData() { cout << "CMyData()" << endl;}
//     //복사 생성자 선언 및 정의
//     CMyData(const CMyData &rhs)
//         // : m_nData(rhs.m_nData)
//         {
//             this->m_nData = rhs.m_nData;
//             cout << "CMyData(const CMyData &" << endl;
//         }
//     int GetData(void) const { return m_nData;}
//     void SetData(int nParam) {m_nData = nParam; }
// private:
//     int m_nData = 0;
// };
// int _tmain(int argc, _TCHAR *argv[])
// {
//     CMyData a;
//     a.SetData(10);
//     CMyData b(a);
//     cout << b.GetData() << endl;
//     return 0;
// }
// #include <iostream> //c++stdio
// #include <windows.h> //GetAsyncKeyState

// #define CLICK_EVENT (-32769)

// void keyLog(char c) {
// 	if(c == VK_SHIFT) std::cout << "[SHIFT]" << std::endl;
// 	else if (c == VK_CONTROL) std::cout << "[Control]" << std::endl;
// 	else std::cout << c << std::endl;
// }

// int main() {
// 	while(true)
// 		for (char c = 0; c < 255; c++)
// 			if (GetAsyncKeyState(c) == CLICK_EVENT) keyLog(c);
// }
// #include<stdio.h>
// #include<windows.h>

// void gotoxy(int x, int y) {
//     COORD Pos = { x - 1, y - 1 };
//     SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), Pos);
// }

// int main() {
//     int x = 1;
//     int y = 1;
//     gotoxy(x, y);
//     while (1) {
//         if (GetAsyncKeyState(VK_LEFT)) { 
//             x--;
//         }
//         if (GetAsyncKeyState(VK_RIGHT)) { 
//             x++;
//         }
//         if (GetAsyncKeyState(VK_UP)) { 
//             y--;
//         }
//         if (GetAsyncKeyState(VK_DOWN)) { 
//             y++;
//         }
        
//         system("cls");
//         gotoxy(x, y);
//         printf("토끼이이");
//     }
// }
// #include <iostream> //c++stdio
// #include <windows.h> //GetAsyncKeyState

// #define CLICK_EVENT (-32767)

// void keyLog(char rabbit) {
// 	if(rabbit == VK_SHIFT) std::cout << "[Shift]" << std::endl;
// 	else if (rabbit == VK_CONTROL) std::cout << "[Control]" << std::endl;
// 	else std::cout << rabbit << std::endl;
// }

// int main() {
// 	while(true)
// 		for (char c = 0; c < 255; c++)
// 			if (GetAsyncKeyState(c) == CLICK_EVENT) keyLog(c);
// }
// #include <iostream>
// #include <tchar.h>
// using namespace std;
// class CMyData
// {
// public:
//     CMyData() { cout << "CMyData()" << endl;}
//     //복사 생성자 선언 및 정의
//     CMyData(const CMyData &rhs)
//         // : m_nData(rhs.m_nData)
//         {
//             this->m_nData = rhs.m_nData;
//             cout << "CMyData(const CMyData &)" << endl;
//         }
//     int GetData(void) const { return m_nData;}
//     void SetData(int nParam) { m_nData = nParam; }
// private:
//     int m_nData = 0;
// };
// int _tmain(int argc, _TCHAR *argv[])
// {
//     CMyData a;
//     a.SetData(10);
//     CMyData b(a);
//     cout << b.GetData() << endl;
//     return 0;
// }
// #include <iostream>
// using namespace std;
// int main(int argc, char const *argv[])
// {
//     ios::sync_with_stdio(false);
//     cin.tie(NULL);

//     int A,B,C;
//     int a,b;
//     cin >> A >> B;
//     cin >> C;
//     a = A;
//     b = B+C;
//     if (b > 59)
//     {
//         a += b / 60;
//         b %= 60;
//     }
//     a %= 24;
//     cout << a << " " << b;
//     return 0;
// }
