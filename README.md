# AiBD_pawelmanka

Readme lab_2:
Celem ćwiczenia jest pobranie i uporządkowanie przydzielonego zbioru danych zgodnie z protokołem TIER i zasadami "tidy data". 
Uporządkowanie badań temperatury wybraych 5 miesięcy 2010 roku.

1. Zgodnie z zasadami TIER stworzyłem 4 osobne:
  1.1 command_files_folder - plik który zawiera skrypt
  1.2 documents - ktory zawiera pliki dokumentacji w tym README
  1.3 original_data - który zawiera dane oryginalne w formacie txt
  
2. Podjęte działania:
  2.1 Początkowo pobrałem dane z odpowiedniego repozytorium. Nie dało się bezpośrednio przekonwertować,za pomocą funkcji df.read_csv(), danych do odpowiedniego dataframu (była tylko jedna kolumna) dlatego jest to robione za pomocą pętli for. Dane musiały zostać poddane slicingu.
  2.2 Aby zyskać informację o danych pobrałem dokumentacje ze strony: https://www.ncei.noaa.gov/products/land-based-station/global-historical-climatology-network-daily
  
