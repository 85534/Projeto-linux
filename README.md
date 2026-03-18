 Projeto-linux
Projeto de bruta força no linux

Wordlist:
123456
senha123
admin
12345678
qwerty
abc123
123123
admin123
root
toor

Scripts:

import json
from utils import carregar_wordlist


with open('../config/config.json') as f:
    config = json.load(f)

wordlist = carregar_wordlist(config["wordlist"])

print("Wordlist carregada:", len(wordlist), "palavras")


for senha in wordlist[:10]:
    print("Testando:", senha)


configuracoes:
{
  "wordlist": "../wordlists/senhas.txt",
  "modo": "teste",
  "threads": 5
}










