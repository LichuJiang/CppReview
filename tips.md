```c++
int a=5;
int b=3;
double c=a/b;//答案会是1
double c=static_cast<double>(a)/b;//答案为1.66667
```



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
