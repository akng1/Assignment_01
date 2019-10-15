#include <iostream>

using namespace std;


 /**tripleByValue函数通过按值传递传递了count的一份副本，把该副本的值增至3倍并返回这一结果。**/
/**tripleByReference函数通过一个引用参数来对count进行按引用传递，通过别名(即引用参数)把
count原来的值增至3倍。**/

double tripleByValue(double count)//按值传递 
{
    count = 3*count;
    return count;
}
double tripleByReference(double &count)//按引用参数传递 
{
    count = count*3;
    return count;
}

int main()
{
    double count;
    cout << "请输入一个整数：" << endl;
    cin >> count;
    cout << "按值传递的结果为：" << tripleByValue(count) << endl;
    cout << "请输入一个整数：" << endl;
    cin >> count;
    cout << "按引用传递的结果为：" << tripleByReference(count) << endl;
    return 0;
}
