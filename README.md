// ConsoleApplication1.cpp: 定义控制台应用程序的入口点。
//


#include <iostream>
#include <cstdio>
#include <cstdlib>
#include <vector>

using namespace std;

int map[31][31];
int n;
bool vi[31][31];
int mx[] = { 1,0 }, my[] = { 0,1 },rmx[] = {0,-1}, rmy[] = {-1,0};

int dfs(int i, int j, int now,int fx)
{
	if (fx == 1)
	{
		if (!vi[i][j])
		{
			now += map[i][j] ;
		}
		if ( (i == n - 1 && j == n - 1))
		{
			now += map[i][j];
		}
	}
}


int main()
{
	scanf_s("%d", &n);
	for (int i = 0; i < n; i++)
	{
		for (int j = 0; j < n; j++)
		{
			scanf_s("%d", &map[i][j]);
		}
	}
	return 0;
}

/*int m[4] = { 3,-1,1,-3 },maxd;
bool isok = false;
string now, to;
vector<char>ans;
vector<long long>ha;
map<int, char>mp;

bool same(string a,string b)
{
	for(int i=0;i<9;i++)
	if(a[i]!=b[i])
	return false;
	return true;
}
void swap(int a, int b)
{
	char x = now[a];
	now[a] = now[b];
	now[b] = x;
}
void f(int no,int pre=-1,int d=0)
{
	if(pre+1)
	{
		swap(no, pre);
		ans.push_back(mp[no - pre]);
	}
	if (d == maxd)
	{
		if (same(now,to))
			isok = true;
		else
		{
			if(pre+1)
			swap(no, pre);
			ans.pop_back();
		}
		return;
	}
	for (int i = 0; i < 4; i++)
	{
		if (isok)
			return;
		if(no+m[i]<0||no+m[i]>=9)
		continue;
		f(no + m[i], no, d + 1);
	}
	if(isok)
	return;
	if(pre+1)
	{
		ans.pop_back();
		swap(no, pre);
	}
}

int main()
{
	mp[3] = 'd';
	mp[1] = 'r';
	mp[-3] = 'u';
	mp[-1] = 'l';
	int n;
	cin >> n;
	for (int i = 0; i < n; i++)
	{
		isok=false;
		cin >> now >> to;
		int x;
		for (x = 0; x < 9; x++)
		{
			if (now[x] == 'X')
			{
				break;
			}
		}
		for (maxd = 1;; maxd++)
		{
			f(x,-1,0);
			if (isok)
				break;
		}
		printf("Case %d: %d\n", i + 1, maxd);
		for (int i = 0; i < ans.size(); i++)
		{
			if (i)
				cout<<" ";
			cout<<ans[i];
		}
		puts("");
	}
	return 0;
}

*/
