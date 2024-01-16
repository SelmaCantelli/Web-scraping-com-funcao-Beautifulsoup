# Webscraping-com-fun-o-Beautifulsoup
O web scraping (raspagem de rede, em tradução livre), também conhecido como extração de dados da web, é o nome dado ao processo de coleta de dados estruturados da web de maneira automatizada. 
# Importar bibliotecas
import requests
from bs4 import BeautifulSoup

import requests
from bs4 import BeautifulSoup


# Coletar a primeira página da lista de artistas
page = requests.get('https://web.archive.org/web/20121007172955/https://www.nga.gov/collection/anZ1.htm')

import requests
from bs4 import BeautifulSoup


page = requests.get('https://web.archive.org/web/20121007172955/https://www.nga.gov/collection/anZ1.htm')

# Criar o objeto BeautifulSoup
soup = BeautifulSoup(page.text, 'html.parser')

import requests
from bs4 import BeautifulSoup


# Coletar e analisar a primeira página
page = requests.get('https://web.archive.org/web/20121007172955/https://www.nga.gov/collection/anZ1.htm')
soup = BeautifulSoup(page.text, 'html.parser')

# Pegar todo o texto da div BodyText
artist_name_list = soup.find(class_='BodyText')

# Pegar o texto de todas as instâncias da tag <a> dentro da div BodyText
artist_name_list_items = artist_name_list.find_all('a')

...
artist_name_list = soup.find(class_='BodyText')
artist_name_list_items = artist_name_list.find_all('a')

# Criar loop para imprimir todos os nomes de artistas
for artist_name in artist_name_list_items:
    print(artist_name.prettify())
