# Biblioteca Digitale

## Descrizione
Questa applicazione consente la gestione di una biblioteca digitale, 
permettendo agli utenti di consultare i libri disponibili, 
registrarsi e accedere con nome e password, prendere in prestito libri e restituirli. 
Gli amministratori possono gestire il catalogo dei libri e monitorare gli utenti.

## Funzionalità principali
- Consultazione del catalogo dei libri disponibili.
- Registrazione e autenticazione degli utenti.
- Prestito e restituzione dei libri con tracciamento delle date.
- Modalità amministratore per la gestione del catalogo.
- Gestione degli utenti registrati.
- Gestione degli amministratori con accesso a funzionalità avanzate.

## Struttura dei file
- **libri.txt**: Contiene l'elenco dei libri disponibili nel formato:
  ```
  Titolo, Autore, ISBN
  ```
  **Esempio:**
  ```
  Il Signore degli Anelli, J.R.R. Tolkien, 9780544003415
  1984, George Orwell, 9780451524935
  ```

- **utenti.txt**: Contiene l'elenco degli utenti registrati con credenziali nel formato:
  ```
  Nome, Password
  ```
  **Esempio:**
  ```
  Mario Rossi, password123
  ```

- **amministratori.txt**: Contiene l'elenco degli amministratori con credenziali nel formato:
  ```
  Nome, Password
  ```
  **Esempio:**
  ```
  Admin1, admin123
  ```

- **prestiti.txt**: Contiene i prestiti attivi nel formato:
  ```
  Nome Utente, ISBN Libro, Data Prestito, Data Scadenza, (Data Restituzione "facoltativa")
  ```
  **Esempio:**
  ```
  Mario Rossi, 9780544003415, 2025-02-18, 2025-02-21
  ```
