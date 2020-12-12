import re
import requests
from itertools import groupby

link = "https://pastebin.com/raw/7543p0ns" #вставляем имя сайта, с которого хотим взять все ссылки

sitetext = requests.get(link).text # запро


pattern = r'<a.*?href=".*?:\/\/((?:\w|-)+(?:\.(?:\w|-)+)+)' # шаблон

links = re.findall(pattern, sitetext) #поиск по шаблону

links = sorted(links) #сортировка сайтов

new_link = [el for el, _ in groupby(links)] #если есть повторяющиеся сайты, оставляем только 1 экземпляр

for link in new_link:
    print(link)
