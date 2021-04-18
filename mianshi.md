## Lambda表达式
- 语言更加简洁
- 逻辑更加清晰
- 编译器可能会将之内联展开
- 当lambda表达式完全由一条return语句组成时才能进行自动类型推断，否则要制定返回值类型。
 
        auto func = [](double x)->double {double y = 5.0; return x / y; };
- 按值访问[x],按引用访问 [&], 按值访问[=]
- 