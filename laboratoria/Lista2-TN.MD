# Lista 2 - tydzień nieparzysty

1. Wykonaj krok po kroku  część 1 listy 2 z eportalu
2. Zapoznaj się z częścią 2  listy 2 z eportalu, zaimplementuj opisaną aplikację
3. Zaimplementuj SWOJE WŁASNE zadanie obliczeniowe wykorzystująć szkielet aplikacji opisany na eportalu ( punkt 2):
	Modyfikacja:

	- Jedna aplikacja która może się uruchaiać w trybie workera lub farmera (jeden main,  bez kopiowania kodu)
	- Uruchamiamy farmer + co najmniej 4 workerów (liczba workerów ma być konfigurowalna)
	- Zadnie dzielone jest na n workerów i uruchamiane, a następnie wynik jest łączony na farmerze 
	- Do uruchomienia zadania wykorzystaj parallel streams (lub inną metodę pozwalającą uruchomić zadania równocześnie na wszystkich workerach)
	- Przykłady zadań:
		- Gregory-Leibniz PI (każdy worker oblicza przedział ciągu)
		- Nilakantha Pi (każdy worker oblicza przedział ciągu)
		- Merge sort (każdy worker sortuje 1/n część tablic, farmer łączy wyniki sortowania)
		- ...

4. Na zajęciach konieczna będzie nieznaczna modyfikacja programu kluczowa dla zaliczenia zadania. 


## Modyfikacja na zajęciach

1. Każdy worker oprócz wyniku ma zwracać czas obliczeń (od otrzymania zadania do przesłania wyniku)
2. "Farmer" ma wypisywać czas który zajęły obliczenia (od przesłania zadania do pierwszego workera, do otrzymania ostatniego wyniku), czasy workerów oraz średni czas workera
3. Daj możliwość specyfikacji czy zadania mają być uruchamiane na workerach sekwencyjnie czy równolegle (pytanie przy uruchomieniu farmera)