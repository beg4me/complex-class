# complex-class
/* nothing <br> feeling low..
well its a very basic program by which we can add and multiply complex numbers:

dont laugh   */

#include <iostream>
using namespace std;
class complex{
private:
   int real;
   int img;

public:
    complex (int real,int img)
    {
  this->real=real;
  this->img=img;

    }
    void add(complex c2)
    {

        int r=this->real+c2.real;
        int i=this->img+c2.img;
         // now we will create a function to store the values;
         this->real=r;
         this->img=i;

    }
    void multiply(complex c2)
    {
     int r=(this->real*c2.real)-(this->img*c2.img);
     int i=(this->real*c2.img)+(this->img*c2.real);

        // store this values in complex 1

        this->real=r;
        this->img=i;
    }
    void print()
    {
        cout<<"("<<real<<")"<<"+"<<"i"<<"("<<img<<")"<<endl;
    }
};
int main()
{

    int real1,img1,real2,img2;
    cout<<"enter the real and imaginary part for complex 1:";
    cin>>real1>>img1;
    cout<<"enter the real and imaginary part for complex 2:";
    cin>>real2>>img2;

   complex c1 (real1,img1);
   complex c2 (real2,img2);

   int choice;
   cout<<"enter ur choice:";
   cin>>choice;

   if(choice==1)
   {
       c1.add(c2);
       c1.print();
   }
   else if(choice==2)
   {
      c1.multiply(c2);
       c1.print();
   }
   else {
    return 0;
   }

}


