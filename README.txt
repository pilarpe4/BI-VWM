# BI-VWM
1/ corpus, dokumenty 10.000 - .txt soubory
2/ slova seřadit podle počtu a vyhodit nejcastejsi
3/ stemovani a lematizace
4/ tvorba tabulky
5/ GUI
6/ parsování dotazu - gramatika ETF
7/ ukázání výsledků

NOT -1 - váha
pro dotaz pro termy najdeme relevantni ID (vaha > 0) a na ty dokumenty spocitame vahu a podle ni pak seradime dokumenty a vypiseme

fukce projde všechny dokumenty a pujde slovo po slovu, slovo porovna s nasimi ukazkovymi slovy takže 1. sloupec 
	jestli ta neni, tak neresime a jdeme dal, 
	pokud tam je tak se podivam do druheho sloupce vezme to slovo a to zapise do tabulky do sloupecku s lemmaty. ke svému dokumentu zapíšu 1 a u ostatní předchozích 0.

z toho udelame spojaky / tabulku a ta se zapise na disk.

term: idd1/vaha -> idd2/vaha -> idd5/vaha ...
.
.
......................................... ...

fukce vezme input
parsovani dotazu pomoci gramatiky 

pes AND dog --> operand/ped operator/AND operand/dog --> ped dog AND --> funkce pro AND provede operaci...

https://en.wikipedia.org/wiki/Reverse_Polish_notation	
https://www.geeksforgeeks.org/stack-set-2-infix-to-postfix/
https://www.textfixer.com/tutorials/common-english-words.txt -----stop words?
https://tartarus.org/martin/PorterStemmer/c_thread_safe.txt  -----stemming, porter algorithm
http://lemmatise.ijs.si/                                     -----lemmatizer	

https://www.corpusdata.org/formats.asp - dokumenty

složka words - obsahuje soubor words.txt
složka data - obsahuje dokumenty (syntax: doc1.txt), plus soubor docsCount.txt - obsahuje jen jeden integer, ktery udava pocet dokumentu

TODO fillDocumentTable.cpp - vše tam je, jen chybí přepis seznamu do souboru (easy). Jen co StopSlova? Našel jsem link výše s frekventovanými slovy: buď vyšrktneme z words.txt nebo nějak zahrnu do programu
