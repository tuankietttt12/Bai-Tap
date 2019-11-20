#include <bits/stdc++.h>

#define tichcheo(a, b) (a.x*b.y - a.y*b.x)
#define tichdodai(a, b) ((sqrt(a.x*a.x + a.y*a.y))*(sqrt(b.x*b.x + b.y*b.y)))
#define tichvohuong(a, b) (a.x*b.x + a.y*b.y)
#define dodai(a) (sqrt(a.x*a.x + a.y*a.y))

using namespace std;

struct Point{
	float x, y;
};

Point A, B, C, D, AC, AB, DC, res, DA, DB, CA, CB, CD, BD, AD, BC;
float d, Dk, Dl, k, l;
int t = 0;

Point Creat(Point A, Point B){
	Point k;
	k.x = B.x - A.x;
	k.y = B.y - A.y;
	return k;
}
bool F(Point A, Point B){
	if (A.x == B.x && A.y == B.y) return true;
	else
		return false;
}

int main()
{
    cin >> A.x >> A.y >> B.x >> B.y >> C.x >> C.y >> D.x >> D.y;
    AB = Creat(A, B);
    DC = Creat(D, C);
    AC = Creat(A, C);
    DA = Creat(D, A);
    DB = Creat(D, B);
    CA = Creat(C, A);
    CB = Creat(C, B);
    CD = Creat(C, D);
    BD = Creat(B, D);
    AD = Creat(A, D);
    BC = Creat(B, C);
    d = tichcheo(AB, DC);
    Dk = tichcheo(AC, DC);
    Dl = tichcheo(AB, AC);
    k = Dk/d;
    l = Dl/d;
    cout << fixed;
	cout.precision(1);
    if (d != 0){
		if (k >= 0 && l >= 0 && k <= 1 && l <= 1){
			cout << "YES" << endl;
			res.x = A.x + k*(B.x - A.x);
			res.y = A.y + k*(B.y - A.y);
			cout << res.x << " " << res.y;
		}
		else
			cout << "NO";
    }
    else{
		if ((F(A, C) && F(B, D)) || (F(A, D) && F(B, C))){
			t = 1;
			cout << "Trung";
		}
		else{
            if (F(A, C))
				if (tichdodai(DA, DB) == tichvohuong(DA, DB)){
					if (dodai(DA) == dodai(DC)){
						t = 1;
						cout << "YES" << endl;
						cout << A.x << " " << A.y;
					}
				}
				else{
					t = 1;
					cout << "Trung";
				}
			if (F(B, C))
				if (tichdodai(DA, DB) == tichvohuong(DA, DB)){
					if (dodai(DB) == dodai(DC)){
						t = 1;
						cout << "YES" << endl;
						cout << B.x << " " << B.y;
					}
				}
				else{
					t = 1;
					cout << "Trung";
				}
			if (F(A, D))
				if (tichdodai(CA, CB) == tichvohuong(CA, CB)){
					if (dodai(CA) == dodai(CD)){
						t = 1;
						cout << "YES" << endl;
						cout << A.x << " " << A.y;
					}
				}
				else{
					t = 1;
					cout << "Trung";
				}
			if (F(B, D))
				if (tichdodai(CA, CB) == tichvohuong(CA, CB)){
					if (dodai(CB) == dodai(CD)){
						t = 1;
						cout << "YES" << endl;
						cout << B.x << " " << B.y;
					}
				}
				else{
					t = 1;
					cout << "Trung";
				}
		}
		if (tichvohuong(AC, BC) <= 0 || tichvohuong(AD, BD) <= 0 ||
		   (tichvohuong(AC, BC) <= 0 && tichvohuong(AD, BD) <= 0) ||
			tichvohuong(AC, BD) <= 0){
			if (t == 0){
				cout << "Trung";
				t = 1;
			}
		}
		if (t == 0) cout << "NO";
    }
    return 0;
}
