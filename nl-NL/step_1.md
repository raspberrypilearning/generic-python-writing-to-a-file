- Gegevens naar een bestand schrijven met Python is heel eenvoudig. Eerst heb je wat gegevens nodig om te schrijven. Hier wordt het opgeslagen als een variabele met de naam `tekst`.

    ```python
    tekst = 'Dit zijn enkele gegevens om te schrijven'
    ```

- De volgende stap is het openen van een bestand. Je moet de naam van het bestand doorgeven aan de functie `open`. De functie moet ook weten met welke **modus** het bestand wordt geopend. Hier is de modus `w`, wat staat voor "schrijven" (write).

    ```python
    f = open('mijn_document.txt', 'w', encoding="utf-8")
    ```
- Vervolgens kunnen de gegevens naar het bestand worden geschreven.

    ```python
  f.write(tekst)
  ```

- Ten slotte moet het bestand worden gesloten.

  ```python
  f.close()
  ```

- Een andere manier om dit te doen is om het bestand automatisch te **sluiten** door het trefwoord `with`. Dit heeft vaak de voorkeur, omdat het gemakkelijk is om te vergeten het bestand **te sluiten**.

  ```python
  tekst = 'Dit zijn enkele gegevens om te schrijven'
with open('mijn_document.txt', 'w', encoding="utf-8") as f:
    f.write(tekst)
  ```
