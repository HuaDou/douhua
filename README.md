# README  

# TEXT_PROCESSOR  
Text_processor is a small text preprocessor.The main function is to preprocess the text for fixed typesetting.The text processor is very simple now, it's unable to handle characters other than whitespace and Englis characters.  

### Declaration of class  
```
class text_processor  
{  
    public:  
        string process(const string &text, unsigned long width);  
    private:  
        string segment_lines(int start_line,int end_line);  
        bool check_text(const string &text);  
        bool check_width(unsigned long width);  
        bool is_Alpha(char ch);  
};  
 ```    
 

### Exception 
1.Invaild characters：Characters other than whitespace and Englis characters. Return "ERROR: Invalid character detected!".  
2.Width out of range：Width should be in [10,80],otherwise return "ERROR: Width out of range!".    
## Build  
`$ cd text_processor `  
`$ g++ -std=c++11 text_processor.cpp -o text_processor`  


## Run  
For example usage: text_processor width text  
  
`$ ./text_processor 30 "The main theme of education in engineering school is learning to teach yourself"`  
