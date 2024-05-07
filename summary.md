1.Mysql encoding mistake: change ur sql files'encode to 'latin1'

2.in C++， using c_str() to locate the address of a string, Eg:printf('%s', a.c_str()) //while using printf('%s', a), but [string a = 'anystring'], then willnot print anytihng

3.The <<C plus prime vol.6>> has a tough problem in 6.16 for me at the first begining, number 5. coding a pymorid like
A
ABA
ABCBA
ABCDCBA
(while you get this func a 'D')
when I suddenly realize this could be simplfiy to an math problem, but didn't using any resource on any froum, though I make this within 40 mins:

//solving the outside, making sure 1,2,3,4,5……sequal
    
    int a,b,c;
    a=5;
    for(b=0;b<=a;b++){
        for(c=a-b;c<=a;c++){
        printf("%d",a-c);
    }
        printf("\n");
    }

//inside, which took me at least 30 mins to figure how to make them interating without messing up with the main loop
    
    int a,b,c;
    a=5;
    for(b=0;b<=a;b++){
        for(c=a-b;c<=a;c++){
        printf("%d",a-c);
    }
        printf("\n");
    }

combine these 2 together:

    char let = '（any A-Z or other ACSII characters）';
    char start;
    char start2;
    char end;
    for(end = 'A';end <= let;end++){
        for(start ='A';start<= end;start++){
            printf("%c",start);  
        }
        /*you should put this 2 fotrloops including in the big loop, ！！！instad of Nesifying them ！！！*/
        for(start2 = let-end+'A';start2 < let;start2++){
            printf("%c",let-start2+'A'-1);  
        }
    printf("\n");  
    }


4.include<math.h> in cpp always has alot surprises:
 1.pow(x,y) while you using "^" as to get numbers's squares, it will leads to some mistakes due to the unsolving Binary prolems, such case you can solve the problem by using a function name pow(oringal number, square number)
 2.fomd(x,y) when you want to get the deviding left number, using '%' on any integer is corect, but when you meet float, you can using fmod(x, y) for problems solvig, which wouldn't making mistakes as possible than the formet one.

5.differences between [ getchar() and scanf() ]
    when using scanf() (without specific situation like:you make some codition youself), it will stop while reading notchar type characters like '\n'、' '(space), which getchar()willnot, bcs getchar() read one char at once. based on that, you can using both functs but using getchar() after scanf() for "clearing the '\n' in the buffer" in case of program reconize you need to judge some codition, or using getchar() all the time to aviod them.
    getchar() using Ctrl+Z to stop reading.It don't need any parameter, so you can code like this : putchar(getchar()); it means print user's input.

6.STL::iterator
    Iterator can be seemed as pointer, it could be gainter any types like 
    
      std::vector<int> myvector;    //codes on cppoffical
      for (int i=1; i<=5; i++) myvector.push_back(i);
      
      std::cout << "myvector contains:";
      for (std::vector<int>::iterator it = myvector.begin() ; it != myvector.end(); ++it)
      std::cout << ' ' << *it;
      std::cout << '\n';
    '''
 





