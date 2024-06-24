# PYTHON-PROGRAM-5
class distance:
    def __init__(self):
        self.km=0
        self.m=0
    def set(self,km,m):
        self.km=km
        self.m=m
    def __isub__(self,distance):
        self.m=self.m-distance.m
        if self.m<0:
            self.m+=1000
            self.km+=1
        self.km=self.km-distance.km
        return self
    def convert_to_meters(self):
        return (self.km*1000+self.m)
    def display(self):
        print(self.km,"kilometers",self.m,"meters")
d1=distance()
d2=distance()
d1.set(21,70)
d2.set(18,120)
d1-=d2
print("d1-d2:")
d1.display()
print("that is:",d1.convert_to_meters(),"meters")
end
class complex:
    def __init__(self):
        self.real=0
        self.img=0
    def setvalue(self,real,img):
        self.real=real
        self.img=img
    def __add__(self,val):
        temp=complex()
        temp.real=self.real+val.real
        temp.img=self.img+val.img
        return temp
    def display(self):
        print("(",self.real,'+',self.img,'i'")")
val1=complex()
val2=complex()
val3=complex()
val1.setvalue(1,2)
val2.setvalue(3,4)
val3=val1+val2
val3.display()
end
