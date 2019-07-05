# Homework
____________________________________
Given a string, divide it to consective groups of same value
E.g input: 111222aabbb#
=> 111   222  aa bbb #
E.g. Input HHHH
=> HHHH (just 1 group)


____________________________________


    
    #include <bits/stdc++.h>
    #include <iostream>
    using namespace std;
    int main()
    {
     char str[100] ;
    cin>>str;
        int i = 0, alphabet[26] = {0}, j,w=0,num[10];
    memset(num,0,sizeof(num));
    while (str[i] != '\0')
    {
        if (str[i] >= 'a' && str[i] <= 'z')
        {
            j = str[i] - 'a';
            if(alphabet[j]==0) w++;
                ++alphabet[j];
        }
        else if (str[i] >= '0' && str[i] <= '9')
        {
            j = str[i] - '0';

            if(num[j]==0) w++;
              ++num[j];
        }
        ++i;
    }
    cout<<"Frequency of all alphabets in the string is:"<<endl;
    for (i = 0; i < 26; i++)
        if(alphabet[i]>0)cout<< char(i + 'a')<<" : "<< alphabet[i]<< endl;
    for (i = 0; i < 10; i++) if(num[i]>0)cout<< i<<" : "<< num[i]<< endl;
    cout<< w<< endl;
    return 0;
    }
________________________________________________________________________
Given a string, Convert it to int
E.g. Convert(“156”) => 156
E.g. Convert(“001520”) => 1520 

    #include<bits/stdc++.h>
    using namespace std ;
    int main() 
     {    
    string str1 = "45"; 
    string str2 = "3.14159"; 
    string str3 = "31337 geek"; 
 
    int myint1 = stoi(str1); 
    int myint2 = stoi(str2); 
    int myint3 = stoi(str3); 
 
    cout << "stoi(\"" << str1 << "\") is "
         << myint1 << '\n'; 
    cout << "stoi(\"" << str2 << "\") is "
         << myint2 << '\n'; 
        cout << "stoi(\"" << str3 << "\") is "
         << myint3 << '\n'; 
 
    return 0; 
    }
________________________________________________________________________
