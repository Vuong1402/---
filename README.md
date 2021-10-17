#include <iostream>
#include <cstring>
int i,k,a[104],b[104],x,n2,n,sum;
char  s1[104],s2[104];
using namespace std;
int main() {
    cin.getline(s1,100,'\n'); 
    cin.getline(s2,100,'\n');
    for (int i=0; i<strlen(s1); ++i) 
    {   
        if (isdigit(s1[i])) 
        { 
            x=x*10+int(s1[i])-int('0'); 
        } 
        if ((s1[i]==' ') or (i==strlen(s1)-1)) 
        { 
            ++n; 
            a[n]=x; 
            x=0; 
            for (int j=1; j<=n; j++) 
                if (a[n]<a[j]) 
                    swap(a[n],a[j]); 
        } 
    } 
    n2=0; 
    for (int i=0; i<strlen(s2); ++i) 
    { 
        if (isdigit(s2[i])) 
    { 
        x=x*10+int(s2[i])-int('0'); 
    } 
        if ((s2[i]==' ') or (i==strlen(s2)-1)) 
    { 
        ++n2; 
        b[n2]=x; 
        x=0; 
        for (int j=1; j<=n2; j++) 
        if (b[n2]>b[j]) 
        swap(b[n2],b[j]); 
    } 
    } 

    sum=0; 
    for (int i=1; i<=n; i++) 
        sum=sum+a[i]*b[i]; 
    cout<<sum;  
    return 0;
}
          ![Screenshot (133)](https://user-images.githubusercontent.com/90500831/137639714-d4ad321c-3b6c-4cd0-9fe4-81d63484681b.png)
    ![Screenshot (134)](https://user-images.githubusercontent.com/90500831/137639716-c7bcb7b5-206e-492f-810a-ea44a4c421bb.png)
