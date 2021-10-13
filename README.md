# Readme lab_2

Readme lab_2:
Celem ćwiczenia jest pobranie i uporządkowanie przydzielonego zbioru danych zgodnie z protokołem TIER i zasadami "tidy data". 
Uporządkowanie badań temperatury wybraych 5 miesięcy 2010 roku.

1. Zgodnie z zasadami TIER stworzyłem 4 osobne:
  1.1 command_files_folder - plik który zawiera skrypt
  1.2 documents - ktory zawiera pliki dokumentacji w tym README
  1.3 original_data - który zawiera dane oryginalne w formacie txt
  
2. Podjęte działania:
  *2.1 Początkowo pobrałem dane z odpowiedniego repozytorium. Nie dało się bezpośrednio przekonwertować,za pomocą funkcji df.read_csv(), danych do odpowiedniego dataframu (była tylko jedna kolumna) dlatego jest to robione za pomocą pętli for. Dane musiały zostać poddane slicingu.
  *2.2 Aby zyskać informację o danych pobrałem dokumentacje ze strony: https://www.ncei.noaa.gov/products/land-based-station/global-historical-climatology-network-daily
  *2.3 Na podstawie dokumentacji udało mi się znaleźć powtarzalność w pliku weather.txt: Na tej podstawie da się zauważyć:
      (UWAGA - znaki w nawiasach są podane jak dla slicingu w tablicy python]:
      *2.3.1 [0:11] znaków to ID
      *2.3.2 [11:15] znaków to rok
      *2.3.3 [15:17] znaków to miesiąc 
      *2.3.4 [17:21] to zmienne badana (n = 0)
      *2.3.5 [21] + 8n to znak "-" pojawiający się przy 9999
      *2.3.6 [22:26] + 8n to wartość badanej zmiennej 
      *2.3.7 [26:29] + 8n miejsce poświęcone na flagi
      *2.3.8. [29] to znak "-" (n+= 1 wróć do 2.3.5)
      *2.3.9. wykonuj aż skończy się pojedynczy wiersz
  *2.4 Po zastosowaniu powyższego algorytmu dla całej tabeli stworzyłem DataFrame. 
  *2.5 Następnie z powyższego DataFramu zastosowałem TidyData i stworzyłem tabele o następujących kolumnach:
      ID, ID_stacji, Rok, miesiąc, Dzień, Tmax, Tmin, PRCP, Flaga 
      
