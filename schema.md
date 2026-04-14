## tabella: dipartimenti
- id ( INT, PRIMARY KEY, AUTO_INCREMENT )
- nome ( VARCHAR(100), NOT NULL )
- descrizione ( TEXT )


## tabella: corsi_laurea

- id ( INT, PRIMARY KEY, AUTO_INCREMENT )
- dipartimento_id ( INT )
- nome ( VARCHAR(150) NOT NULL )
- tipo ( VARCHAR(20) )
- durata_anni ( INT )


## tabella: corsi

- id ( INT, PRIMARY KEY, AUTO_INCREMENT )
- corsi_larea_id ( INT )
- nome ( VARCHAR(150) )
- crediti ( INT )
- anno ( INT )


## tabella: insegnanti

- id ( INT, PRIMARY KEY, AUTO_INCREMENT )
- nome ( VARCHAR(100) )
- cognome ( VARCHAR(100) )
- email VARCHAR(150) UNIQUE,
- ruolo ( VARCHAR(20) )


## tabella: esami

- id ( INT, PRIMARY KEY, AUTO_INCREMENT )
- corsi_id ( INT )
- data ( DATE )
- ora ( TIME )
- aula ( VARCHAR(50) )
- modalità ( VARCHAR(20) )


## tabella: studenti 

- id ( INT, PRIMARY KEY, AUTO_INCREMENT )
- corsi_larea_id ( INT )
- nome ( VARCHAR(100) )
- cognome ( VARCHAR(100) )
- matricola ( VARCHAR(20) UNIQUE )
- data_iscrizione ( DATE )