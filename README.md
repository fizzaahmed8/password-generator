import os, random, string

length = 13
chars = string.ascii_letters + string.digits + '!@#$%^&*()'
random.seed = (os.urandom(1024))

print ''.join(random.choice(chars) for i in range(length))
import random
length=13
ListOfChars=[]
codes=list(range(48,57))+list(range(65,90))+list(range(97,122))
for a in range(length):
    ASCIIcode=random.choice(codes)
    ListOfChars.append(chr(ASCIIcode))
print(''.join(ListOfChars))
import string
import random

def id_generator(size=13, chars=string.ascii_uppercase + string.digits):
    return ''.join(random.choice(chars) for _ in range(size))

print "Your password is: ", id_generator()
def Generate_Password():
    input_ = input('please enter your password: ')
#i saw you have a limit of length 6, but you can tweak it
    if len(input_) > 6:
        print ('Max length for a pssword is 6')
    hashPassword = hashlib.sha3_256(b'{input_}').hexdigest()
    return (hashPassword)
    def check(self):
    #print 'select one\n'
    if self.choice == 1:
        self.genpass()  
    elif self.choice == 3:
        self.exi(exit)
    else:
        print 'invalid entry try again' 
        self.main()
        #print 'invalid'

def genpass(self):
    import random
    import re
    import string 
    min_len = 8
    max_len = 12
    self.passlen = random.randint(min_len, max_len)
    #s = "@4A%1aXb6!B2#8lZ$t5&"
    #random.shuffle(s)
    #password =  "".join(random.sample(s,passlen))
    #print 'Generate password \n', password, '\n'

    self.password1 = ""
    SpecialChars = "!@#$%%^*"
    self.password1 += random.choice(string.ascii_uppercase)
    self.password1 += random.choice(string.ascii_lowercase)
    self.password1 += random.choice(string.digits)
    self.password1 += random.choice(SpecialChars)
    for i in range(0,self.passlen):
        self.password1 += random.choice(string.ascii_uppercase +
          string.ascii_lowercase + 
          string.digits+
          SpecialChars)
    self.all_symbol = ''.join(random.sample(self.password1,self.passlen))
    flag =0
    while True:   
        if not re.search("[a-z]", self.all_symbol): 
            flag = -1
            break
        elif not re.search("[A-Z]", self.all_symbol): 
            flag = -1
            break
        elif not re.search("[0-9]", self.all_symbol): 
            flag = -1
            break
        elif not re.search("[_@$]", self.all_symbol): 
            flag = -1
            break
        elif re.search("\s", self.all_symbol): 
            flag = -1
            break
        else: 
            flag = 0
            print 'password Length\t', self.passlen
            print 'Generate password is\t', self.all_symbol, '\n'
            break

    if flag ==-1: 
        self.genpass()




        #print len(password)
def exi(self, exit):
    import sys
    sys.exit()
