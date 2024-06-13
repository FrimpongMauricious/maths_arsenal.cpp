# maths_arsenal.cpp
#include <iostream>
#include <cmath>
#include<iomanip>
using namespace std;

int main()
{double a,b, c, d,e,f,g,h,i,x1,x2,j, a1,a2,b1,c1,b2,c2,xANS,yANS,yA,xA,yAN,xAN;
   cout<<"************THE MATHS ARSENAL********************"<<endl;
   cout<<"The topics provided below are set of topics in mathematics , u are objective is to select the option under which u want my simple AI to help u solve some simple questions  under it "<<endl;
   cout<<" 1.quadratic equation"<<endl;
   cout<<" 2.equation of a straight line"<<endl;
   cout<<" 3.simultanuouse equation involving two variables "<<endl;
   cout<<" 4.inverse of a 2*2 matrix"<<endl;
  cout<<" 5.inverse of a 3*3 matrix"<<endl;
    cout<<" 6.determinant of a 2*2 matrix"<<endl;
   cout<<" 7. determinant of a 3*3 matrix"<<endl;
   cout<<" 8. equation of the line of bestfit"<<endl;
   cout<<" 9.standard deviation of a set of ungroup data"<<endl;
   cout<<"10.factorial of a number: "<<endl;
   cout<<"11.differentiation: "<<endl<<endl;
   string option;
   cout<<"enter the number assigned to the math topic: ";
   cin>>option;
   if(option=="1"){
        cout<<"enter the value of x(squared): ";
   cin>>a;
   cout<<"enter the value of x: ";
   cin>>b;
   cout<<"enter the constant: ";
   cin>>c;
   cout<<"the quadratic equation written is "<<a<<"x^2 +"<<b<<"x +"<<c<<endl;
   d=pow(b,2)-(4*a*c);
   x1=(-b+sqrt(d))/(2*a);
   x2=(-b-sqrt(d))/(2*a);
   cout<<"the results for the above equation is "<<x1 <<" and "<<" "<<x2;

   }
   else if(option=="3"){
    cout<<"enter the coefficient of x: ";
    cin>>a1;
    cout<<"enter the coefficient of y: ";
    cin>>b1;
    cout<<"enter the first constant: ";
    cin>>c1;
    cout<<"enter the coefficient of x: ";
    cin>>a2;
    cout<<"enter the coefficient of y: ";
    cin>>b2;
    cout<<"enter the second constant: ";
    cin>>c2;
    a1=(-c1-b1)/a1;
    a2=(-c2-b2)/a2;
    yAN=((-a1*c2)+(a2*c1));
yA=((a1*b2)-(a2*b1));
yANS=(yAN)/(yA);
    xAN=(-c1-(b1*yANS));
    xANS=(xAN)/a1;
    cout<<"x= "<<xANS<<" y= "<<yANS;
   }
   if (option=="2"){
    cout<<"***********************EQUATION OF A LINE*********************" <<endl<<endl;

    double A1,A2,m,B1,B2;
    //taking the points from the user
    cout<<"enter the x cordinate of point A: ";
    cin>>A1;
    cout<<"enter the y cordinate of point A: ";
    cin>>A2;
    cout<<"enter the x cordinate of point B: ";
    cin>>B1;
    cout<<"enter the y cordinate of point B: ";
    cin>>B2;
    //done with points entery
    //determining the gradient of the line
    m=(B2-A2)/(B1-A1);
    //printing the equation of the line
    if(B1-A1==0){//checking if the gradient is not infinty
cout<<"the equation of the line does not exist since the gradient can not represented if the change in x value is (zero): ";
    }
    else{
    cout<<"y= "<<m<<"x"<<" + "<<A2+(m*(-A1));
    }
   }
   if(option=="10"){
        cout<<"******************THE FACTORIAL OF A NUMBER********************"<<endl<<endl;
      int num;
   int factorial=1;
   int counter;
   cout<<"enter number: ";
   cin>>num;
   for(counter=num; counter>=2; counter--){
    factorial=factorial*counter;
   }
   cout<<num <<"! " <<" equals " << factorial;
   }
   if(option=="11"){
        double degree,fx1,fx2,fx3;//variables declaration
    cout<<"******************DIFFERENTIATION OF A FUNCTION********************"<<endl<<endl;
    cout<<"enter the highest degree of the function: ";//taking the highest exponent in the function
   cin>>degree;
cout<<"please enter the the coefficients of the terms in descending power of degree. If a term is not present, please just enter zero. Than you!"<<endl<<endl;

cout<<"enter the first term: ";
cin>>fx1;
cout<<"enter the second term of the function: ";
cin>>fx2;
cout<<"enter the next term: ";
cin>>fx3;
cout<<"dy/dx = "<<degree*fx1<<"x^"<<(degree-1)<<" + ";
cout<<(degree-1)*fx2<<"x^"<<(degree-2)<<"+ ";
cout<<"0";

   }
   if(option=="4"){
    double matrix[4];
   double det;

    double transpose;


    for(int i=1; i<=4; i++){
        cout<<"enter the elements row-wise: ";
        cin>>matrix[i];
        det=(matrix[1]*matrix[4])-(matrix[2]*matrix[3]);


    }
    cout<<endl<<endl;
    det=(matrix[1]*matrix[4])-(matrix[2]*matrix[3]);
    cout<<"the determinant of the matrix above is: "<<det<<endl<<endl;
if(det==0){
    cout<<"the inverse of the matrix can not be determined since its determinant is zero: "<<endl<<endl;
}
matrix[2]=-1*matrix[2];
matrix[3]=-1*matrix[3];
double c=matrix[1];
matrix[1]=matrix[4];
matrix[4]=c;
double inverse_1=(1/det)*matrix[1];
double inverse_2=(1/det)*matrix[2];
double inverse_3=(1/det)*matrix[3];
double inverse_4=(1/det)*matrix[4];
cout<<"the adjoint of this 2*2 matrix is "<<endl<<endl;
cout<<matrix[1]<<" "<<matrix[2]<<" "<<endl<<endl;
cout<<matrix[3]<<" "<<matrix[4]<<" "<<endl <<endl;
cout<<"the inverse of the matrix is  as follows: "<<endl<<endl<<endl;
cout<<setprecision(2)<<inverse_1<<setprecision(2)<<" "<<" "<< inverse_2<<setprecision(2)<<" "<<endl<<endl;
cout<< inverse_3<<setprecision(2)<<" "<<" "<<inverse_4<<setprecision(2)<<" "<<endl;
   }
   system("pause>0");
   return 0;
}
