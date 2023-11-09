# Esempi di utilizzo di SED + AWK

### Esempio 1: Estrarre e Formattare Dati
- **File (file1.txt):**
  ```
  Mario Rossi 120 2100
  Luca Bianchi 150 1800
  Giulia Verdi 90 2300
  Anna Neri 110 2000
  Marco Bianchi 200 1600
  Giulia Ferrari 80 2200
  Stefano Gialli 95 2050
  Laura Blu 130 1900
  Fabio Viola 105 2150
  ```

- **Cosa vogliamo fare:** Estrae il nome e il cognome da ogni riga e li separa con una virgola e uno spazio.

- **Output Atteso:**
  ```
  Mario, Rossi
  Luca, Bianchi
  Giulia, Verdi
  Anna, Neri
  Marco, Bianchi
  Giulia, Ferrari
  Stefano, Gialli
  Laura, Blu
  Fabio, Viola
  ```

### Esempio 2: Selezionare Righe e Sostituire Testo
- **File (file2.txt):**
  ```
  Mario Rossi 120 2100
  Luca Bianchi 150 1800
  Giulia Verdi 90 2300
  Anna Neri 110 2000
  Marco Bianchi 200 1600
  Giulia Ferrari 80 2200
  Stefano Gialli 95 2050
  Laura Blu 130 1900
  Fabio Viola 105 2150
  ```

- **Cosa vogliamo fare:** Seleziona righe con "Rossi" e sostituisce "2100" con "modificato".

- **Output Atteso:**
  ```
  Mario Rossi 120 modificato
  ```

### Esempio 3: Numerazione delle Righe e Aggiunta di Testo
- **File (file3.txt):**
  ```
  Mario Rossi
  Luca Bianchi
  Giulia Verdi
  Anna Neri
  Marco Bianchi
  Giulia Ferrari
  Stefano Gialli
  Laura Blu
  Fabio Viola
  ```

- **Cosa vogliamo fare:** Aggiunge un numero di riga all'inizio e " - FINE" alla fine di ogni riga.

- **Output Atteso:**
  ```
  1 Mario Rossi - FINE
  2 Luca Bianchi - FINE
  3 Giulia Verdi - FINE
  4 Anna Neri - FINE
  5 Marco Bianchi - FINE
  6 Giulia Ferrari - FINE
  7 Stefano Gialli - FINE
  8 Laura Blu - FINE
  9 Fabio Viola - FINE
  ```

### Esempio 4: Filtrare e Cambiare il Formato delle Date
- **File (file4.txt):**
  ```
  2023-01-15 Mario Rossi
  2023-02-20 Luca Bianchi
  2023-03-25 Giulia Verdi
  2023-04-10 Anna Neri
  2023-05-05 Marco Bianchi
  2023-06-30 Giulia Ferrari
  2023-07-20 Stefano Gialli
  2023-08-15 Laura Blu
  2023-09-10 Fabio Viola
  ```

- **Cosa vogliamo fare:** Seleziona righe contenenti "Luca" e cambia il formato della data.

- **Output Atteso:**
  ```
  20/02/2023 Luca Bianchi
  ```

### Esempio 5: Aggiungere Contenuto Condizionalmente
- **File (file5.txt):**
  ```
  Mario Rossi 120 2100
  Luca Bianchi 150 1800
  Giulia Verdi 90 
  Anna Neri 110 2000
  Marco Bianchi 200 1600
  Giulia Ferrari 80 2200
  Stefano Gialli 95 2050
  Laura Blu 130 1900
  Fabio Viola 105 2150
  ```

- **Cosa vogliamo fare:** Controlla se il terzo campo è maggiore di 100 e stampa l'intera riga; altrimenti stampa solo nome e cognome con "***". Poi sostituisce "2100" con "SOLD OUT".

- **Output Atteso:**
  ```
  Mario Rossi 120 SOLD OUT
  Luca Bianchi 150 1800
  Anna Neri 110 2000
  Marco Bianchi 200 1600
  Stefano Gialli 95 ***
  Laura Blu 130 1900
  Fabio Viola 105 2150
  ```

### Esempio 6: Eliminare Righe Doppie e Sostituire Testo
- **File (file6.txt):**
  ```
  Mario Rossi
  Luca Bianchi
  Mario Rossi
  Giulia Verdi
  Anna Neri
  Mario Rossi
  Marco Bianchi
  ```

- **Cosa vogliamo fare:** Rimuove righe duplicate e sostituisce "Mario" con "MARCO".

- **Output Atteso:**
  ```
  MARCO Rossi
  Luca Bianchi
  Giulia Verdi
  Anna Neri
  Marco Bianchi
  ```

### Esempio 7: Estrarre Colonne e Sostituire Valori
- **File (file7.txt):**
  ```
  Mario Rossi 120 2100
  Luca Bianchi 150 1800
  Giulia Verdi 90 2300
  Anna Neri 110 2000
  Marco Bianchi 200 1600
  Giulia Ferrari 80 2200
  Stefano Gialli 95 2050
  Laura Blu 130 1900
  Fabio Viola 105 2150
  ```

- **Cosa vogliamo fare:** Estrae il nome e il quarto campo da ogni riga, poi sostituisce "2100" con "REMOVED".

- **Output Atteso:**
  ```
  Mario REMOVED
  Luca 1800
  Giulia 2300
  Anna 2000
  Marco 1600
  Giulia 2200
  Stefano 2050
  Laura 1900
  Fabio 2150
  ```

### Esempio 8: Modificare il Contenuto Basato su Condizioni
- **File (file8.txt):**
  ```
  Mario Rossi 120 2100
  Luca Bianchi 150 1800
  Giulia Verdi 90 2300
  Anna Neri 110 2000
  Marco Bianchi 200 1600
  Giulia Ferrari 80 2200
  Stefano Gialli 95 2050
  Laura Blu 130 1900
  Fabio Viola 105 2150
  ```

- **Cosa vogliamo fare:** Modifica il cognome da "Bianchi" a "ROSSI" se il terzo campo è maggiore di 100, poi cambia "ROSSI" in "REPLACED".

- **Output Atteso:**
  ```
  Mario Rossi 120 2100
  Luca REPLACED 150 1800
  Anna Neri 110 2000
  Marco REPLACED 200 1600
  Laura Blu 130 1900
  Fabio Viola 105 2150
  ```

### Esempio 9: Inserimento Condizionale di Testo
- **File (file9.txt):**
  ```
  Mario Rossi 120 2100
  Luca Bianchi 150 1800
  Giulia Verdi 90 2300
  Anna Neri 110 2000
  Marco Bianchi 200 1600
  Giulia Ferrari 80 2200
  Stefano Gialli 95 2050
  Laura Blu 130 1900
  Fabio Viola 105 2150
  ```

- **Cosa vogliamo fare:** Aggiunge "ALTO: " o "BASSO: " davanti alle righe a seconda del quarto campo, poi cambia "BASSO: Luca" in "ALTERATO: Luca".

- **Output Atteso:**
  ```
  BASSO: Mario Rossi 120 2100
  ALTERATO: Luca Bianchi 150 1800
  ALTO: Giulia Verdi 90 2300
  BASSO: Anna Neri 110 2000
  BASSO: Marco Bianchi 200 1600
  ALTO: Giulia Ferrari 80 2200
  BASSO: Stefano Gialli 95 2050
  BASSO: Laura Blu 130 1900
  ALTO: Fabio Viola 105 2150
  ```
