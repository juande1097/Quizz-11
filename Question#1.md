Quizz-11

#include <iostream>
#include <cmath>
using namespace std;

float calculateE (float n){
float e = 0.0;
float guardar_e;
float resultado = 1000000;
float x = 0.0;
float y = 1.0;
while (resultado > n){
if (x == 0.0){
y = 1.0;
guardar_e = e;
e = e + (1.0/y);
resultado = e - guardar_e;
x++;
}
else {
y = y*x;
guardar_e = e;
e = e + (1.0/y);
resultado = e - guardar_e;
x++;
}
}
return e;
}

int main(){
float n;
cout << "Cuanta precision necesitas"<< endl;
cin>> n;
float e = calculateE (n);
cout << e << endl;
return 0;
}
