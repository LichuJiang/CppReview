```c++
int a=5;
int b=3;
double c=a/b;//答案会是1
double c=static_cast<double>(a)/b;//答案为1.66667
```

尽量用 {}初始化，优点是会有边界检查


```c++
string s{"absdasdasd"};
    if(s.find("is")!=string::npos){
        cout<<"finded";
    }else{
        cout<<"null";
    }
    cout<<endl;
    cout<<string::npos;
    cout<<endl;
    cout<<s.find("is");
```
string::npos代表string的末尾，值为18446744073709551615，如果s.find("is")等于这个末尾值就代表已经找完了也没找到

```c++
string s1="abc";
string s2="bcd";
s2=s1+"bdcsda";//correct
s2="asdasd"+"zxczxczcx";//incorrect
```
c++的string中，+的两端要么全是string，要么一个string一个c风格字符串，不能全是c风格字符串(c style literal)  
pair的使用技巧：  
https://blog.csdn.net/sevenjoin/article/details/81937695  

二进制小技巧：  
将整型数字转化为1：  
```c++
int a=10;
cout<<bitset<8>(a);
//输出00001010
//其中8代表展示多少位
```
计算某个数二进制的形式下有多少个1：  
```c++
int a=10;
bitset<8> foo(a);
cout<<foo.count();
//输出2
```
方法二：  
```c++
int a=10;
int count=__builtin_popcount(a);
cout<<count;
//输出2
```
