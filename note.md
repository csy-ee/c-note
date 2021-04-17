分割字符串<br>

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