import requests
import time
from pystyle import Colors, Colorate
from os import system
from requests import get
import string
from colorama import Fore
import asyncio
from bs4 import BeautifulSoup
from pystyle import Colors, Colorate
from re import search
from secrets import token_hex
import requests,threading,os
from os import system
from time import sleep
from requests import Session
from httpx import get
from colorama import Fore
from time import sleep
from requests import get
from subprocess import check_output
from os import system
from httpx import Client
from pystyle import Add, Center, Anime, Colors, Colorate, Write, System
from sys import stdout
from json import dumps, loads
from random import choice, randint, shuffle
from pystyle import Add, Center, Anime, Colors, Colorate, Write, System
from os.path import isfile, isdir
from py_compile import compile
from os import listdir, mkdir, remove, rmdir, rename, chdir, name
from shutil import move, copy, rmtree
from time import sleep
from binascii import hexlify
from colorama import Fore
from tqdm import tqdm, trange
from time import sleep
from concurrent.futures import ThreadPoolExecutor
from operator import truediv
from httpx import Client
from requests import get
from concurrent.futures import ThreadPoolExecutor
from time import sleep
from subprocess import check_output
import httpx
import requests as ru
import itertools
import threading
import requests
import time
import random
import datetime
import pystyle
import gratient
from time import sleep
from pystyle import Colors, Colorate, Anime, Write
from requests import Session
from re import search
from concurrent.futures import ThreadPoolExecutor
from pystyle import Colors, Colorate
import random
from requests import Session
from re import search
from bs4 import BeautifulSoup as bs
from user_agent import generate_user_agent
from requests import Session,post,get
import threading
import time
import random
import os
import datetime
import sys
import asyncio
from re import search
from requests import Session
from re import search
from bs4 import BeautifulSoup as bs
from user_agent import generate_user_agent
from requests import Session,post,get
from pystyle import Colors, Colorate
from colorama import Fore
import subprocess
import sys
import time
import subprocess
import sys
import time

def dumpper(guildid, des):
    authkey = input("Token : ")
    guildid = input("Copy Guildid : ")
    des = input("Place Guildid : ")
    header = {
        "Authorization": f"{authkey}"
    }
    def rb(text):
        return Colorate.Horizontal(Colors.blue_to_cyan,text)
    def get(url, **args):
        req = requests.get(f"https://discord.com/api/v9{url}", headers=header, **args)
        return req
    def post(url, **args):
        req = requests.post(f"https://discord.com/api/v9{url}", headers=header, **args)
        return req
    def patch(url, **args):
        req = requests.patch(f"https://discord.com/api/v9{url}", headers=header, **args)
        return req
    def get_guild():
        return get(f"/guilds/{guildid}").json()
    def get_roles():
        return get(f"/guilds/{guildid}/roles").json()
    def get_channels():
        return get(f"/guilds/{guildid}/channels").json()
    def clear_server(guild_id):
        def get_all_roles(guild):
            res = requests.get(f"https://discord.com/api/v9/guilds/{guild}/roles", headers=header)
            tab = []
            for i in res.json():
                try:
                    tab.insert(1, i["id"])
                except:
                    pass
            return tab
        def get_all_channels(guild):
            res = requests.get(f"https://discord.com/api/v9/guilds/{guild}/channels", headers=header)
            tab = []
            for i in res.json():
                try:
                    tab.insert(1, i["id"])
                except:
                    pass
            return tab
        def delete_role(guild, role_id):
            res = requests.delete(f"https://discord.com/api/v9/guilds/{guild}/roles/{role_id}", headers=header)
        def delete_channel(guild, ch_id):
            res = requests.delete(f"https://discord.com/api/v9/channels/{ch_id}", headers=header)
        for i in get_all_channels(guild_id):
            delete_channel(guild_id, i)
        for i in get_all_roles(guild_id):
            delete_role(guild_id, i)
        os.system ("cls")
        print(gratient.blue(f"""
โ•”โ•—   โ•”โ•โ•โ•โ•—โ•”โ•โ•โ•โ•—โ•”โ•— โ•”โ•—โ•”โ•โ•โ•โ•—    โ•”โ•โ•โ•โ•—โ•”โ•— โ•”โ•—โ•”โ•โ•โ•โ•—โ•”โ•โ•โ•โ•—
โ•‘โ•‘   โ•‘โ•”โ•โ•—โ•‘โ•‘โ•”โ•โ•—โ•‘โ•‘โ•‘ โ•‘โ•‘โ•‘โ•”โ•โ•—โ•‘    โ•‘โ•”โ•โ•—โ•‘โ•‘โ•‘ โ•‘โ•‘โ•‘โ•”โ•โ•—โ•‘โ•‘โ•”โ•โ•—โ•‘
โ•‘โ•‘   โ•‘โ•โ•โ•โ•‘โ•โ•โ•”โ•โ•‘โ•‘โ•โ•โ•โ•‘โ•‘โ•‘ โ•‘โ•‘    โ•‘โ•โ•โ•โ•—โ•‘โ•โ•โ•โ•‘โ•‘โ•‘ โ•‘โ•‘โ•‘โ•โ•โ•โ•‘
โ•‘โ•‘ โ•”โ•—โ•‘โ•”โ•—โ•”โ•โ•”โ•โ•โ•”โ•โ•โ•โ•โ•—โ•‘โ•‘โ•‘ โ•‘โ•‘    โ•โ•โ•โ•—โ•‘โ•‘โ•”โ•โ•—โ•‘โ•‘โ•‘ โ•‘โ•‘โ•‘โ•”โ•โ•โ•
โ•‘โ•โ•โ•โ•‘โ•‘โ•‘โ•‘โ•โ•—โ•‘โ•‘โ•โ•โ•—   โ•‘โ•‘โ•‘โ•โ•โ•โ•‘    โ•‘โ•โ•โ•โ•‘โ•‘โ•‘ โ•‘โ•‘โ•‘โ•โ•โ•โ•‘โ•‘โ•‘   
โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•   โ•โ•โ•โ•โ•โ•โ•    โ•โ•โ•โ•โ•โ•โ• โ•โ•โ•โ•โ•โ•โ•โ•โ•   
                                                 
       COPY DC      BY : LR240 SHOP
	"""))
    def setting_guild(des):
        os.system ("cls")
        print(gratient.blue(f"""
โ•”โ•—   โ•”โ•โ•โ•โ•—โ•”โ•โ•โ•โ•—โ•”โ•— โ•”โ•—โ•”โ•โ•โ•โ•—    โ•”โ•โ•โ•โ•—โ•”โ•— โ•”โ•—โ•”โ•โ•โ•โ•—โ•”โ•โ•โ•โ•—
โ•‘โ•‘   โ•‘โ•”โ•โ•—โ•‘โ•‘โ•”โ•โ•—โ•‘โ•‘โ•‘ โ•‘โ•‘โ•‘โ•”โ•โ•—โ•‘    โ•‘โ•”โ•โ•—โ•‘โ•‘โ•‘ โ•‘โ•‘โ•‘โ•”โ•โ•—โ•‘โ•‘โ•”โ•โ•—โ•‘
โ•‘โ•‘   โ•‘โ•โ•โ•โ•‘โ•โ•โ•”โ•โ•‘โ•‘โ•โ•โ•โ•‘โ•‘โ•‘ โ•‘โ•‘    โ•‘โ•โ•โ•โ•—โ•‘โ•โ•โ•โ•‘โ•‘โ•‘ โ•‘โ•‘โ•‘โ•โ•โ•โ•‘
โ•‘โ•‘ โ•”โ•—โ•‘โ•”โ•—โ•”โ•โ•”โ•โ•โ•”โ•โ•โ•โ•โ•—โ•‘โ•‘โ•‘ โ•‘โ•‘    โ•โ•โ•โ•—โ•‘โ•‘โ•”โ•โ•—โ•‘โ•‘โ•‘ โ•‘โ•‘โ•‘โ•”โ•โ•โ•
โ•‘โ•โ•โ•โ•‘โ•‘โ•‘โ•‘โ•โ•—โ•‘โ•‘โ•โ•โ•—   โ•‘โ•‘โ•‘โ•โ•โ•โ•‘    โ•‘โ•โ•โ•โ•‘โ•‘โ•‘ โ•‘โ•‘โ•‘โ•โ•โ•โ•‘โ•‘โ•‘   
โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•   โ•โ•โ•โ•โ•โ•โ•    โ•โ•โ•โ•โ•โ•โ• โ•โ•โ•โ•โ•โ•โ•โ•โ•   
                                                 
                                                 
                                                       

                    5%
	"""))
        data = get_guild()
        ico = f'https://cdn.discordapp.com/icons/{data["id"]}/{data["icon"]}.webp'
        lk = requests.get(ico).content
        img = f"data:image/png;base64,{lk}"
        patch(f'/guilds/{des}', json={'name': data['name'], 'icon': img,
                                             'afk_timeout': data['afk_timeout'],
                                             'description': data['description'], 'region': data['region']})
    def setting_roles(des):
        os.system ("cls")
        print(gratient.blue(f"""
 โ•”โ•—   โ•”โ•โ•โ•โ•—โ•”โ•โ•โ•โ•—โ•”โ•— โ•”โ•—โ•”โ•โ•โ•โ•—    โ•”โ•โ•โ•โ•—โ•”โ•— โ•”โ•—โ•”โ•โ•โ•โ•—โ•”โ•โ•โ•โ•—
โ•‘โ•‘   โ•‘โ•”โ•โ•—โ•‘โ•‘โ•”โ•โ•—โ•‘โ•‘โ•‘ โ•‘โ•‘โ•‘โ•”โ•โ•—โ•‘    โ•‘โ•”โ•โ•—โ•‘โ•‘โ•‘ โ•‘โ•‘โ•‘โ•”โ•โ•—โ•‘โ•‘โ•”โ•โ•—โ•‘
โ•‘โ•‘   โ•‘โ•โ•โ•โ•‘โ•โ•โ•”โ•โ•‘โ•‘โ•โ•โ•โ•‘โ•‘โ•‘ โ•‘โ•‘    โ•‘โ•โ•โ•โ•—โ•‘โ•โ•โ•โ•‘โ•‘โ•‘ โ•‘โ•‘โ•‘โ•โ•โ•โ•‘
โ•‘โ•‘ โ•”โ•—โ•‘โ•”โ•—โ•”โ•โ•”โ•โ•โ•”โ•โ•โ•โ•โ•—โ•‘โ•‘โ•‘ โ•‘โ•‘    โ•โ•โ•โ•—โ•‘โ•‘โ•”โ•โ•—โ•‘โ•‘โ•‘ โ•‘โ•‘โ•‘โ•”โ•โ•โ•
โ•‘โ•โ•โ•โ•‘โ•‘โ•‘โ•‘โ•โ•—โ•‘โ•‘โ•โ•โ•—   โ•‘โ•‘โ•‘โ•โ•โ•โ•‘    โ•‘โ•โ•โ•โ•‘โ•‘โ•‘ โ•‘โ•‘โ•‘โ•โ•โ•โ•‘โ•‘โ•‘   
โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•   โ•โ•โ•โ•โ•โ•โ•    โ•โ•โ•โ•โ•โ•โ• โ•โ•โ•โ•โ•โ•โ•โ•โ•   
                                                 
                                                 

                    30%
	"""))
        data = get_roles()
        for i in data:
            if not i['name'] == "@everyone":
                if post(f'/guilds/{des}/roles',json={'name':i['name'],'color':i['color'],'permissions':i['permissions'],'mentionable':i['mentionable']}).status_code == 429:
                    print(rb("[+] Rate Limit"))
                    time.sleep(5)
                    post(f'/guilds/{des}/roles',json={'name':i['name'],'color':i['color'],'permissions':i['permissions'],'mentionable':i['mentionable']})
    def setting_channel(des):
        os.system ("cls")
        print(gratient.blue(f"""
 โ•”โ•—   โ•”โ•โ•โ•โ•—โ•”โ•โ•โ•โ•—โ•”โ•— โ•”โ•—โ•”โ•โ•โ•โ•—    โ•”โ•โ•โ•โ•—โ•”โ•— โ•”โ•—โ•”โ•โ•โ•โ•—โ•”โ•โ•โ•โ•—
โ•‘โ•‘   โ•‘โ•”โ•โ•—โ•‘โ•‘โ•”โ•โ•—โ•‘โ•‘โ•‘ โ•‘โ•‘โ•‘โ•”โ•โ•—โ•‘    โ•‘โ•”โ•โ•—โ•‘โ•‘โ•‘ โ•‘โ•‘โ•‘โ•”โ•โ•—โ•‘โ•‘โ•”โ•โ•—โ•‘
โ•‘โ•‘   โ•‘โ•โ•โ•โ•‘โ•โ•โ•”โ•โ•‘โ•‘โ•โ•โ•โ•‘โ•‘โ•‘ โ•‘โ•‘    โ•‘โ•โ•โ•โ•—โ•‘โ•โ•โ•โ•‘โ•‘โ•‘ โ•‘โ•‘โ•‘โ•โ•โ•โ•‘
โ•‘โ•‘ โ•”โ•—โ•‘โ•”โ•—โ•”โ•โ•”โ•โ•โ•”โ•โ•โ•โ•โ•—โ•‘โ•‘โ•‘ โ•‘โ•‘    โ•โ•โ•โ•—โ•‘โ•‘โ•”โ•โ•—โ•‘โ•‘โ•‘ โ•‘โ•‘โ•‘โ•”โ•โ•โ•
โ•‘โ•โ•โ•โ•‘โ•‘โ•‘โ•‘โ•โ•—โ•‘โ•‘โ•โ•โ•—   โ•‘โ•‘โ•‘โ•โ•โ•โ•‘    โ•‘โ•โ•โ•โ•‘โ•‘โ•‘ โ•‘โ•‘โ•‘โ•โ•โ•โ•‘โ•‘โ•‘   
โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•   โ•โ•โ•โ•โ•โ•โ•    โ•โ•โ•โ•โ•โ•โ• โ•โ•โ•โ•โ•โ•โ•โ•โ•   
                                                 
                                                 

                    70%
	"""))
        data = get_channels()
        def get_parent():
            array = []
            for i in data:
                if i['type'] == 4:
                    res = post(f'/guilds/{des}/channels',json={'name': i['name'],'type':i['type'],'position':i['position']})
                    if res.status_code == 429: 
                        print(rb("[+] Rate Limit"))
                        time.sleep(5.5)
                        dt = post(f'/guilds/{des}/channels',json={'name': i['name'],'type':i['type'],'position':i['position']})
                        array.insert(1,str(dt.json()["id"])+":FS:"+str(i["id"]))
                    else:
                        array.insert(1,str(res.json()["id"])+":FS:"+str(i["id"]))
            return array
        def fake_int(text):
            try:    return int(text)
            except:     
                if text == "None":  
                    return None
        parentdata = get_parent()
        for i in data:
            try:   pid = next((element for element in parentdata if i['parent_id'] in element), "None").split(":FS:")[0]   
            except:   pass
            if i['type'] == 0:
                res = post(f'/guilds/{des}/channels',json={'name': i['name'],'type':i['type'],'position':i['position'],'nsfw':i['nsfw'],'rate_limit_per_user':i["rate_limit_per_user"],'parent_id':fake_int(pid)})
                if res.status_code == 429: 
                    print(rb(f"[+] Rate Limit"))
                    time.sleep(int(res.json()['retry_after'])+0.5) 
                    post(f'/guilds/{des}/channels',json={'name': i['name'],'type':i['type'],'position':i['position'],'nsfw':i['nsfw'],'rate_limit_per_user':i["rate_limit_per_user"],'parent_id':fake_int(pid)})
            elif i['type'] == 2:
                res = post(f'/guilds/{des}/channels',json={'name': i['name'],'type':i['type'],'position':i['position'],'bitrate':i['bitrate'],'user_limit':i["user_limit"],'parent_id':fake_int(pid)})
                if res.status_code == 429: 
                    print(rb(f"[+] Rate Limit"))
                    time.sleep(int(res.json()['retry_after'])+0.5) 
                    post(f'/guilds/{des}/channels',json={'name': i['name'],'type':i['type'],'position':i['position'],'bitrate':i['bitrate'],'user_limit':i["user_limit"],'parent_id':fake_int(pid)})
            elif i['type'] == 4:
                pass
            else:
                res = post(f'/guilds/{des}/channels',json={'name': i['name'],'type':i['type'],'position':i['position'],'parent_id':fake_int(pid)})
                if res.status_code == 429: 
                    print(rb(f"[+] Rate Limit"))
                    time.sleep(int(res.json()['retry_after'])+0.5)  
                    post(f'/guilds/{des}/channels',json={'name': i['name'],'type':i['type'],'position':i['position'],'parent_id':fake_int(pid)})
    clear_server(des)
    setting_guild(des)
    setting_roles(des) 
    setting_channel(des)
    os.system ("cls")
    print(gratient.blue(f"""
 โ•”โ•—   โ•”โ•โ•โ•โ•—โ•”โ•โ•โ•โ•—โ•”โ•— โ•”โ•—โ•”โ•โ•โ•โ•—    โ•”โ•โ•โ•โ•—โ•”โ•— โ•”โ•—โ•”โ•โ•โ•โ•—โ•”โ•โ•โ•โ•—
โ•‘โ•‘   โ•‘โ•”โ•โ•—โ•‘โ•‘โ•”โ•โ•—โ•‘โ•‘โ•‘ โ•‘โ•‘โ•‘โ•”โ•โ•—โ•‘    โ•‘โ•”โ•โ•—โ•‘โ•‘โ•‘ โ•‘โ•‘โ•‘โ•”โ•โ•—โ•‘โ•‘โ•”โ•โ•—โ•‘
โ•‘โ•‘   โ•‘โ•โ•โ•โ•‘โ•โ•โ•”โ•โ•‘โ•‘โ•โ•โ•โ•‘โ•‘โ•‘ โ•‘โ•‘    โ•‘โ•โ•โ•โ•—โ•‘โ•โ•โ•โ•‘โ•‘โ•‘ โ•‘โ•‘โ•‘โ•โ•โ•โ•‘
โ•‘โ•‘ โ•”โ•—โ•‘โ•”โ•—โ•”โ•โ•”โ•โ•โ•”โ•โ•โ•โ•โ•—โ•‘โ•‘โ•‘ โ•‘โ•‘    โ•โ•โ•โ•—โ•‘โ•‘โ•”โ•โ•—โ•‘โ•‘โ•‘ โ•‘โ•‘โ•‘โ•”โ•โ•โ•
โ•‘โ•โ•โ•โ•‘โ•‘โ•‘โ•‘โ•โ•—โ•‘โ•‘โ•โ•โ•—   โ•‘โ•‘โ•‘โ•โ•โ•โ•‘    โ•‘โ•โ•โ•โ•‘โ•‘โ•‘ โ•‘โ•‘โ•‘โ•โ•โ•โ•‘โ•‘โ•‘   
โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•โ•   โ•โ•โ•โ•โ•โ•โ•    โ•โ•โ•โ•โ•โ•โ• โ•โ•โ•โ•โ•โ•โ•โ•โ•   
                                                 
                                                 
                   () 100% เน€เธชเธฃเนเธเนเธฅเนเธงเธเธฃเธฑเธ ()

	"""))
    en = input("Enter To Close..")
dumpper("1176915786070237315", "1189862377265582140")
