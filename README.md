# Biblioteca Digitale

## Descrizione
Questa applicazione consente la gestione di una biblioteca digitale, 
permettendo agli utenti di consultare i libri disponibili, 
registrarsi e accedere con nome e password, prendere in prestito libri e restituirli. 
Gli amministratori possono gestire il catalogo dei libri e monitorare gli utenti.
### Login e registrazione utenti
Un utente che lancia l’applicazione può effettuare il login (o come utente o come amministratore) oppure registrare un nuovo account (solo utente). Le credenziali di accesso degli utenti sono scritte in un file di testo. La registrazione di account amministratore avviene modificando direttamente il file esternamente (non tramite l’interfaccia utente del programma).

### Utente normale
Dopo essersi loggato come utente, è possibile:
- visualizzare la lista dei libri in catalogo, ognuno con le disponibilità attuali
- visualizzare la lista dei libri in prestito, evidenziando in maniera particolare i prestiti scaduti
- prendere un libro in prestito: se il libro è disponibile, verrà generata una prenotazione, segnando la data del prestito. Dopo aver
- prenotato il libro, il programma mostra all’utente un codice di prenotazione, che sarà mostrato dall’utente al personale della biblioteca per recuperare la prenotazione e prendere effettivamente il libro in prestito.
- estendere il prestito: di norma il libro in prestito va restituito entro un mese, ma l’utente che ha un libro in prestito, prima della scadenza di quest’ultimo, può estendere la prenotazione per un altro mese a partire dalla data di scadenza del prestito attuale 

### Utente amministratore
Dopo essersi loggato come amministratore, è possibile:
- aggiungere un altro amministratore (aggiungendone le credenziali di accesso al relativo file)
- visualizzare la lista dei libri in catalogo
- aggiungere o rimuovere copie di libri in catalogo
- visualizzare lo storico dei prestiti di un libro specifico (dal più recente al più vecchio)
- visualizzare lo storico dei prestiti di un cliente specifico (dal più recente al più vecchio)
- chiudere un prestito: quando il cliente della biblioteca restituisce un libro, mostrandone il numero di prenotazione, l’amministratore può chiudere il prestito, rendendo nuovamente disponibile la copia per altri clienti della biblioteca.


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
  Codice prenotazione, Nome Utente, ISBN Libro, Data Prestito, Data Scadenza, (Data Restituzione "facoltativa")
  ```
  **Esempio:**
  ```
  12345678, Mario Rossi, 9780544003415, 2025-02-18, 2025-02-21
  ```
