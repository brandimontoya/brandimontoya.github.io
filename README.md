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
    s
## represents humans
class Human {    
  protected:      
    int height;    
    int weight; 
    int age;
    string name; 
    string profession;
    string gender;
   public:
   	void seth(int h);
   	void setw(int w);
   	void seta(int a);
   	void setn(string n);
   	void setp(string p);
	void setg(string g);
};

## class inherited from Human
class Criminal: public Human {
  protected:
    string crime;
 public:
    setc(string c);
};
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
CREATE TABLE Student (ID varchar(10), Subject varchar(10), Marks int, FOREIGN KEY (ID) REFERENCES Registry(ID)) ;

CREATE TABLE Teacher (ID varchar(10), Subject varchar(10), FOREIGN KEY (ID) REFERENCES Registry(ID)) ;

CREATE TABLE OtherStaff (ID varchar(10), Job varchar(10), FOREIGN KEY (ID) REFERENCES Registry(ID)) ;

CREATE TABLE Registry (Name varchar(10),ID int, Role varchar(10), Age int, DOB datetime, Address varchar(20), Telephone varchar(10), PRIMARY KEY (ID));

INSERT INTO Registry
	(Name, ID, Role, Age, DOB, Address, Telephone)
VALUES
    ('Randall', 1, 'Student', 12, '11-12-2008', '16 Watery Lane', '2824258'),
    ('Beck', 2, 'Student', 12, '15-11-2008', '12 Western Lane', '7924288'),
    ('Kathy', 3, 'Student', 12, '1-9-2008', '65 Westminster Alley', '4527259'),
    ('Dave', 4, 'Student', 12, '10-1-2008', '15 Airy Gardens', '7854258'),
    ('Emily', 5, 'Student', 12, '20-2-2008', '24 Watery Lane', '9844728'),
    ('Gwen', 6, 'Student', 12, '7-12-2008', '10 Cady Colony', '6443256'),
    ('Missy', 7, 'Teacher', 42, '5-5-1978', '70 Ruddy Alley', '7654248'),
    ('Gwen', 8, 'Teacher', 35, '7-10-1985', '11 Tech Colony', '8384294'),
    ('Barbara', 9, 'OtherStaff', 56, '7-12-1964', '19 Cady Colony', '4327688')
;


INSERT INTO Student 
	(Name, Subject, Marks)
VALUES
    (1, 'Maths', 35),
    (2, 'Maths', 21),
    (3, 'Maths', 30),
    (4, 'Chemistry', 75),
    (5, 'Chemistry', 45),
    (6, 'Humanities', 15)
;

INSERT INTO Teacher
	(ID, Subject)
VALUES
    (7, 'Humanities'),
    (8, 'Maths')
;

INSERT INTO OtherStaff
	(ID, Job)
VALUES
    (9, 'Receptionist')
;

SELECT ID, Subject, Marks
FROM(
  SELECT ID, Subject, Marks, ROW_NUMBER()OVER(PARTITION BY Subject ORDER BY Marks DESC) theRank
    FROM Class
)X
WHERE theRank = 1

SELECT Name FROM Student WHERE Marks>40
;

SELECT * FROM Registry WHERE Age>35
;

SELECT * FROM Registry WHERE Age>35





