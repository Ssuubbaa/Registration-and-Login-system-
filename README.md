# Registration-and-Login-system-
def register():
  db=open("database.txt","r")
  emailid = input('create emailid:')
  password = input('create password:')
  password1 = input('confirm password:')
  d=[]
  f=[]
  for i in db:
    a,b = i.split(",")
    b=b.strip()
    d.append(a)
    f.append(b)
  data=dict(zip(d,f))
  print(data)
  if password != password1:
    print("password don't match")
    register()
  else:
    if len(password)<5:
      print("password is too short")
      register()
    elif emailid in db:
        print("emailid exists")
        register()
    else:
          db=open("database.txt","a")
          db.write(emailid+','+password+"\n")
          print("sucess")
    register()
    def accesss():
      db=open("database.txt","r")
      emailid = input('create emailid:')
      password = input('create password:')
      password1 = input('confirm password:')
     if len(password)<5
  d=[]
  f=[]
  for i in db:
    a,b = i.split(",")
    b=b.strip()
    d.append(a)
    f.append(b)
  data=dict(zip(d,f))
 try:
 if data(emailid):
  try:
    if password==data[emailid]:
      print("login sucess")
    else:
      print("password incorrect")
   def home(option=none):
      option=input('login|signup)
      if option=="login"
    access()
      elif option=="signup":
      register()
      else:
      print("please enter an option")
     home()
