### **分割字符串**<br>

    vector<string> split(const string& s,const char flag = ' ')
    {
        vector<string> strs;
        istringstream iss(s);
        string temp;
        while (getline(iss, temp, flag)) 
        {
            strs.push_back(temp);
        }
        return strs;
    }

-----
### **产生随机数**<br>


    vector<int> nums(10);
	generate(nums.begin(), nums.end(), rand);

generate接受一个区间（参数1，参数2）， 并将每个元素设置为第三个参数的返回值。第三个参数是一个函数对象。

-----
### **根据条件计数**<br>

    vector<int> nums{1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
	int divby3 = count_if(nums.begin(), nums.end(), [](int x) {return x % 3 == 0; });
	cout << divby3 << endl;

count_if 在一个区间内（参数1， 参数2），计算让参数3返回true的元素的个数。参数3是函数对象。

-----
### **for_each**
	vector<int> nums{ 1, 2, 3, 4, 5 };
	for_each(nums.begin(), nums.end(), [](int& x) {x++; return; });
-----
### **函数符**<br>
（有点像python中的闭包，带超参的函数？）

    class Add
    {
        int inc;
    public:
        Add() { inc = 1; }
        Add(int _inc) : inc(_inc) {}
        int operator()(int x)
        {
            return x + inc;
        }
    };
    int main()
    {
        Add add(3);
        int ret = add(5);
        cout << ret << endl;//8
    }