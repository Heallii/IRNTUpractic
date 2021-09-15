#include <iostream>     
#include <iomanip>       
#include <ctime>    
using namespace std;
 int main()
{
    setlocale(LC_ALL, "Russian");
    srand(time(NULL));
 
    int N, i;
    int choice;
    int *arr = new int [N];
    
    
    cout << "Введите количество элементов массива:";
    cin >> N;
    if ((N > 20) || (N <1))
    {
        cout << " Неподходящий под условие ввод элементов массива " << endl;
    }
    else
    {
        cout << "Как будет заполняться массив ?" << endl;
        cout << "Рандомный ввод - напечатайте 1" << endl;
        cout << "Ручной ввод - напечатайте 2" << endl;
        cin >> choice;
        
        if ((choice > 2) || (choice <1))
        {
        cout << "Неправильно указан способ ввода элементов массива" << endl;
        }
        else{
             if (choice == 2)
              for (int i=0; i < N; i++)
              {
                  cout<<"A["<<i+1<<"]=";
                  cin >> arr[i];
                  cout<<'\n';
              }
        if (choice == 1)
          for (int i = 0; i < N; i++)
        {
            arr[i] = -20+rand()%(39);
                                                 
        }  
    for (int i = 0; i < N; i++)
        {
            cout << "|" << arr[i] << "|";        
        }  
    
    cout << endl;
    cout << "---------------------------------------";
    cout << endl;
    cout << "Изменённый массив: ";
    int j = 0;
    for (int i = 0; i < N; i++)
    {   
        if (arr[i] % 2 != 0)
        {
            j++;
        }
    }
    int *A=new int[j];
    j=0;
        for (int i = 0; i < N; i++)
    {   
        if (arr[i] % 2 != 0)
        {
            A[j]=arr[i];
            cout << "|" << A[j] << "|";   
            j++;
            
        }
    }
    }
}
}
