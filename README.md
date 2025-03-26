# NTPD3 - Gabriela Myszkowiak, grupa 1

Przesłane pliki:
* model.pkl - zapisany plik z modelem
* model.py - plik odpowiedzialny za tworzenie modelu: podział na zbiory, trening, zapis modelu
* app.py - właściwa aplikacja, obsługa endpoint'ów

# Endpoint'y:
* / - realizuje zadanie 1, zwraca przywitanie w formacie json
  ![image](https://github.com/user-attachments/assets/b9455122-0313-47fc-889a-2351b3ce4bb6)

* /predict - zwraca predykcję modelu. Jeśli chcemy otrzymać odpowiedź musimy przesłać dane w formacie json - w tym samym formacie model zwraca odpowiedź. Predykcją modelu jest przynależność do danej klasy.
  Widok w postman:
  ![image](https://github.com/user-attachments/assets/970f498b-69d8-4fbf-aec3-94598718fc47)
  Widok w cURL:
  ![image](https://github.com/user-attachments/assets/bb1107d9-e049-4739-97e0-f77388e5e526)
  Oba sprawdzenia zwracają ten sam wynik

* /predict - obsługa błędów dla zadania nr 3. W przypadku przesłania błędnych danych (np. wybrakowanych) otrzymujemy komunikat
  ![image](https://github.com/user-attachments/assets/e2bde94e-39d9-447e-bc58-4f138fe4e921)

* /info - zwraca informacje o modelu (zad. 4)
  ![image](https://github.com/user-attachments/assets/b44cf67a-c9f2-41ce-8aff-cc4352e2f3fa)

* /health - zwraca informacje o stanie serwera (zad. 4)
  ![image](https://github.com/user-attachments/assets/9ba6b848-b4ea-42d1-8453-804c7b640213)

# Zadanie 5
Ze względu na brak kompatybilności Gunicorn z systemem Windows używam Waitress. Aplikacja działa na porcie 8080
  ![image](https://github.com/user-attachments/assets/a5be0655-ed12-485b-a301-a415a9c95fcb)
