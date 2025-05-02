# Ram-
import mysql.connector 
mydb=mysql.connector.connect(host="localhost",user="root",passwd="manager",database="quiz_comp") 
mycursor=mydb.cursor() 
mycursor.execute("create table questions1(qno_no int(3) primary key , qno_desc varchar(10000),opt_a varchar(500), opt_b varchar(500), opt_c varchar(500) ,opt_d varchar(500) , ans varchar(5000))") 
print("QUIZ SOFTWARE") 
print("1.questions") 
print("2.participants") 
print("3.scores update") 
print("4.display") 
choice=int(input("enter your wish:"))   
 sql_in= "insert into questions1 values(" + str( sql) + ",'" + (sql1)+ "'"+",'" + (sql2) + "'"+",'" + (sql3) +"'" +",'"+ (sql4) +"'"+",'" + (sql5) +"'"+ ",'"+(sql6) +"'"")" 
 mycursor.execute(sql_in) 
  mydb.commit() 
  print("your request has been processed.Thank you for making us as a part of your project") 
 #mycursor.execute("create table participants(reg_no int(5) primary key, pname varchar(50) ,age_group int(10),city varchar(50),no_of_appearances_made int(10))") 
if choice==2: 
    sql6=int(input("enter the participant reg_no:")) 
    sql7=input("enter the participant name:") 
    sql8=int(input("enter the age group:")) 
    sql9=input("enter the city:") 
   sql10=int(input("enter the no of appearances made:")) 
#mycursor.execute("create table scores(reg_no int(5) primary key , participant_name varchar(50),scores int(50),total_correct int(50),total_wrong int(50),total_attempted int(50))") 
if choice==3: 
    a=int(input("enter the reg_no")) 
    b=input("enter the participants name") 
    c=int(input("enter the scores")) 
    d=int(input("enter the total correct answer")) 
    e=int(input("enter the incorrect answer")) 
    f=int(input("enter the no_of_attempted_questions")) 
sql_insert="insert into scores values("+ str(a) +",'"+ (b) +"'"+",'"+ str(c)+"'"+",'"+ str(d) +"'"+ ",'"+str(e) +"'"+",'"+ str(f)+ "'"")" 
    print(sql_insert) 
    mycursor.execute(sql_insert) 
    mydb.commit() 
if choice==4: 
    mycursor.execute("select * from questions1") 
    data=mycursor.fetchall() 
    print(data) 
