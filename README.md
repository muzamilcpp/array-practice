# array-practice:
//Void type function is just called and in integer and float or in which there is something returning we assign the function to a value and then cout it like  : 1-int max=maxvalueinarr( arr,  size).2-cout<<endl<<"Maximum value in a array is: "<<max;
#include <iostream>
using namespace std;
//function for initalization of array
void intilaziearr( int arr[],int size){
    cout<<"Enter the array Elements: "<<endl ;
    for(int i=0;i<size;i++){
        cin>>arr[i];
    }
    
}
//function for diplay of array
void displayarr(int arr[],int size){
    cout<<"The array elements you enterd is: "<<endl ;
    for(int i=0;i<size;i++){
        cout<<arr[i]<<" ";
    }
    
}
//function for sum of array
int sumofarr(int arr[],int size){
    int sum=0;
     for(int i=0;i<size;i++){
       sum+=arr[i];
    }
    return sum;
    
}
//function for of arrayAverage 
float avgofarr(int arr[],int size){
    float sum=0, avg;//to have answer also in float
     for(int i=0;i<size;i++){
       sum+=arr[i];
     
    }
   avg=sum/size;
    return avg;
}
//function for finding maximum value of array
int maxvalueinarr(int arr[], int size) {
    int max = arr[0];
    for (int i = 1; i < size; i++) {
        if (arr[i] > max) {
            max = arr[i];
        }
    }
    return max;
}
//function for finding minimum value of array
int minvalueinarr(int arr[], int size) {
    int min = arr[0];
    for (int i = 1; i < size; i++) {
        if (arr[i] < min) {
            min = arr[i];
        }
    }
    return min;
}

int main() {
  const int size=10;// declaring the size of array it could be of any size
  int arr [size]; 
  
intilaziearr(arr,size);//calling the above function while calling in cpp arguments type and brackets of array is not mentioned
displayarr(arr,size);

int sum = sumofarr(arr,size);
cout<<endl<<"Sum of array: "<<sum;
    

float avg= avgofarr( arr, size)  ;
cout<<endl<<"Average of array: "<<avg;
int max=maxvalueinarr( arr,  size);
cout<<endl<<"Maximum value in a array is: "<<max;
int min=minvalueinarr( arr,  size);
cout<<endl<<"Minimum value in a array is: "<<min;

    return 0;
}
