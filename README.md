#include<iostream.h>
#include<conio.h>
class distance
{
private:
  int km;
  int m;
public:
  void input ();
  void display ();
  distance addition (distance a, distance b);
};
void distance::input ()
{
  cout << "enter km" << endl;
  cin >> km;
  cout << "enter m" << endl;
  cin >> m;
}
void distance::display ()
{
  cout << "km is " << km << endl;
  cout << "m is " << m << endl;
}
distance distance::addition (distance a, distance b)
{
  distance d;
  d.m = a.m + b.m;
  d.km = a.km + b.km + d.m / 1000;
  d.m = d.m % 1000;
  return (d);
}

void
main ()
{
  distance d1, d2, d3;
  d1.input ();
  d2.input ();

  d1.display ();
  d2.display ();

  d3 = d3.addition (d1, d2);
  d3.display ();
  getch ();
}
