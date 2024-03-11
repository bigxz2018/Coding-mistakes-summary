Mysql encoding mistake: change ur sql files'encode to 'latin1'

in C++， using c_str() to locate the address of a string, Eg:printf('%s', a.c_str()) //while using printf('%s', a), but [string a = 'anystring'], then willnot print anytihng

The <<C plus prime vol.6>> has a tough problem in 6.16 for me at the first begining, number 5. coding a pymorid like
A
ABA
ABCBA
ABCDCBA
(while you get this func a 'D')
when I suddenly realize this could be simplfiy to an math problem, but didn't using any resource on any froum, though I make this within 40 mins:
{
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
}
combine these 2 together:

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
