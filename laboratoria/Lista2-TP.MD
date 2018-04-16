# Lista 2 - tydzień parzysty

1. Wykonaj krok po kroku  część 1 listy 2 z eportalu
2. Zapoznaj się z częścią 2  listy 2 z eportalu, zaimplementuj opisaną aplikację
3. Zaimplementuj SWOJE WŁASNE zadanie obliczeniowe wykorzystująć szkielet aplikacji opisany na eportalu ( punkt 2):
	Modyfikacja:

	- Jedna aplikacja która może się uruchaiać w trybie workera lub farmera (jeden main, bez kopiowania kodu)
	- Uruchamiamy farmer + co najmniej 3 workerów (liczba workerów ma być konfigurowalna)
	- Zadnie dzielone jest na n workerów i uruchamiane sekwencyjnie, a następnie wynik jest łączony na farmerze
	- Przykłady zadań:
		- Gregory-Leibniz PI (każdy worker oblicza przedział ciągu)
		- Nilakantha Pi (każdy worker oblicza przedział ciągu)
		- Merge sort (każdy worker sortuje 1/n część tablic, farmer łączy wyniki sortowania)
		- ...

4. Na zajęciach konieczna będzie nieznaczna modyfikacja programu kluczowa dla zaliczenia zadania.


## Modyfikacja na zajęciach

1. "Farmer" oprócz zadania ma przesyłać do workerów losową liczbę
2. Każdy worker oprócz wyniku ma zwracać losową liczbę wyznaczoną wykorzystując liczbę od farmera jako ziarno
3. "Farmer" ma wypisywać średnią wartość losowych liczb oraz ich wartości dla każdego workera