# README

## 代码的构建  

### 对象的声明  
```
class text_processor  
{  
    public:  
        string process(const string &text, unsigned long width);  
    private:  
        string Int_to_String(int start_line,int end_line);  //求出 节 所在行
        bool check_text(const string &text);  //判断 文本 是否含有非法字符
        bool check_width(unsigned long width); //判断 宽度 是否超出范围 
        bool is_Alpha(char ch); //判断 字符 是否为英文字母 
};  
 ```  
### 异常处理  
1.非法字符：能识别出文本中除大小写英文以外的非法字符，返回并在窗口提示“ERROR: Invalid character detected!”.  
2.宽度超出范围：能辨别宽度是否在[10,80]区间内，如果不在，则返回且在窗口提示：“ERROR: Width out of range!”.  

## 如何在Linux中运行  
运用命令行，先进入到 text_process.cpp 目录下，再分别执行以下两条命令：  
1.编译 text_processor.cpp 文件，得到 text_processor 文件  
`g++ -std=c++11 text_processor.cpp -o text_processor`  
2.执行 text_processor 文件,其中 命令行的第二个参数为 宽度， 第三个参数为 文本  
`./text_processor 30 "The main theme of education in engineering school is learning to teach yourself"`  
