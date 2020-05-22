## Hola Amigos

Welcome to my website. This is my ePortfolio for the 499 class, this contains a description of my skillset and projects that I've completed before.

### Software Design and Engineering

Here I include a sample application which I had developed earlier to simulate the variety in human population. I used the object oriented paradigm for this. I have attached some of the relevant code below.

```markdown
class Male {    
  private:      
    int height;    
    int weight; 
    int age;
    string name; 
    string profession;
   public:
   	void seth(string h);
   	void setw(string w);
   	void seta(string a);
   	void setn(string n);
   	void setp(string p);
};

class Female {    
  private:      
    int height;    
    int weight; 
    int age;
    string name; 
    string profession;
   public:
   	void seth(string h);
   	void setw(string w);
   	void seta(string a);
   	void setn(string n);
   	void setp(string p);
};

class Criminal{    
  private:      
    int height;    
    int weight; 
    int age;
    string name; 
    string profession;
    string crime;
   public:
   	void seth(string h);
   	void setw(string w);
   	void seta(string a);
   	void setn(string n);
   	void setp(string p);
   	void setc(string c);
};
```

### Data Structures and Algorithms

Here I include a sample application which I had developed earlier which is a warning system for fraudulent account activity. I used simple data structure like arrays and algos like merge sort. I have attached some of the relevant code below.

```markdown
int main(){
	int N;
	cin>>N;
	int A[N];
	int k;
	cin>>k;

	for(int i=0;i<N;i++){
		cin>>A[i];
	}

	for(int i=k;i<N;i++){
		int a[k];
		for(int j=0;j<k;j++){
			a[j]=A[i-k+j];
		}
		mergesort(a, k);

		float med;
		if(k%2==0){
			med = (a[k/2 - 1] +a[k/2])/2;
		}
		else{
			med = a[k/2];
		}
		if(A[i]>med){
			// cout<<med<<endl;
			cout<<"index "<<i<<endl;
			cout<<"fraud withdraw warning";
			break;
		}
	}

	return 0;
}
```
### Databases

Here I include an sql application which I had developed earlier which is simulates class ranking for exams. Here is a sample.

```markdown
SELECT Name, Subject, Marks
FROM(
  SELECT *, ROW_NUMBER()OVER(PARTITION BY Subject ORDER BY Marks DESC) c
    FROM Class
)X
WHERE c = 1
```




