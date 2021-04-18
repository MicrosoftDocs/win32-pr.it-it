---
title: Errori di registrazione e ripristino nelle funzioni di Active Directory Domain Services
description: In questo argomento vengono elencati i valori restituiti da errori di registrazione e ripristino per le funzioni in Active Directory Domain Services.
ms.assetid: b927073a-8bbc-45d4-b9d3-25f3aa6c6f53
ms.tgt_platform: multiple
keywords:
- AD Active Directory errori di registrazione e ripristino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6fba921a63eb399d6ed4f44ef8569ed05370403
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297725"
---
# <a name="logging-and-recovery-errors-in-functions-in-active-directory-domain-services"></a>Errori di registrazione e ripristino nelle funzioni di Active Directory Domain Services

In questo argomento vengono elencati i valori restituiti da errori di registrazione e ripristino per le funzioni in Active Directory Domain Services.



| Valore                                | Descrizione                                                                                                                      |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **hrLogFileCorrupt**                 | Il file di log è danneggiato.                                                                                                         |
| **hrNoBackupDirectory**              | Non è stata specificata alcuna directory di backup.                                                                                                   |
| **hrBackupDirectoryNotEmpty**        | La directory di backup non è vuota.                                                                                               |
| **hrBackupInProgress**               | Il backup è attivo.                                                                                                                |
| **hrMissingPreviousLogFile**         | Manca un file di log per il checkpoint.                                                                                        |
| **hrLogWriteFail**                   | Impossibile scrivere nel file di log.                                                                                                 |
| **hrBadLogVersion**                  | La versione del file di registro non è compatibile con la versione del database del servizio directory Windows NT/Windows 2000 (NTDS). |
| **hrInvalidLogSequence**             | Il timestamp nel log successivo non corrisponde a quello previsto.                                                                 |
| **hrLoggingDisabled**                | Il log non è attivo.                                                                                                           |
| **hrLogBufferTooSmall**              | Il buffer del log è troppo piccolo per essere recuperato.                                                                                     |
| **hrLogSequenceEnd**                 | È stato superato il numero massimo di file di log.                                                                               |
| **hrNoBackup**                       | Nessun backup in corso.                                                                                                  |
| **hrInvalidBackupSequence**          | La chiamata di backup è fuori sequenza.                                                                                              |
| **hrBackupNotAllowedYet**            | Non è possibile eseguire subito un backup.                                                                                                  |
| **hrDeleteBackupFileFail**           | Impossibile eliminare il file di backup.                                                                                                |
| **hrMakeBackupDirectoryFail**        | Impossibile creare una directory temporanea di backup.                                                                                     |
| **hrInvalidBackup**                  | Non è possibile eseguire un backup incrementale quando è abilitata la registrazione circolare.                                                      |
| **hrRecoveredWithErrors**            | Sono stati rilevati errori durante il processo di ripristino.                                                                               |
| **hrMissingLogFile**                 | Manca il file di registro corrente.                                                                                                 |
| **hrLogDiskFull**                    | Disco di registro pieno.                                                                                                            |
| **hrBadLogSignature**                | Un file di log è danneggiato.                                                                                                           |
| **hrBadDbSignature**                 | Un file di database è danneggiato.                                                                                                      |
| **hrBadCheckpointSignature**         | Un file del checkpoint è danneggiato.                                                                                                    |
| **hrCheckpointCorrupt**              | Un file del checkpoint non è stato trovato o è danneggiato.                                                                       |
| **hrDatabaseInconsistent**           | Il database è danneggiato.                                                                                                         |
| **hrConsistentTimeMismatch**         | Mancata corrispondenza dell'ultima ora coerente del database.                                                                      |
| **hrPatchFileMismatch**              | Il file di correzione non viene generato da questo backup.                                                                                |
| **hrRestoreLogTooLow**               | Il numero di log iniziale è troppo basso per il ripristino.                                                                              |
| **hrRestoreLogTooHigh**              | Il numero di log iniziale è troppo elevato per il ripristino.                                                                             |
| **hrGivenLogFileHasBadSignature**    | Il file di log scaricato dal nastro è danneggiato.                                                                                |
| **hrGivenLogFileIsNotContiguous**    | Impossibile trovare un file di log obbligatorio dopo il download del nastro.                                                               |
| **hrMissingRestoreLogFiles**         | I dati non vengono ripristinati completamente perché mancano alcuni file di log.                                                               |
| **hrExistingLogFileHasBadSignature** | Il file di log nel percorso del file di log è danneggiato.                                                                                    |
| **hrExistingLogFileIsNotContiguous** | Impossibile trovare un file di log obbligatorio nel percorso del file di log.                                                                        |
| **hrMissingFullBackup**              | Il database ha perso un backup completo precedente prima del backup incrementale.                                                        |
| **hrBadBackupDatabaseSize**          | Le dimensioni del database di backup devono essere un multiplo di 4000 (4096 byte).                                                                |
| **hrTermInProgress**                 | È in corso l'arresto del database.                                                                                                 |
| **hrFeatureNotAvailable**            | La funzionalità non è disponibile.                                                                                                    |
| **hrInvalidName**                    | Il nome non è valido.                                                                                                             |
| **hrInvalidParameter**               | Il parametro non è valido.                                                                                                        |
| **hrColumnNull**                     | Il valore della colonna è null.                                                                                                 |
| **hrBufferTruncated**                | Il buffer è troppo piccolo per i dati.                                                                                                |
| **hrDatabaseAttached**               | Il database è già collegato.                                                                                                |
| **hrInvalidDatabaseId**              | ID database non valido.                                                                                                      |
| **hrOutOfMemory**                    | Memoria del computer esaurita.                                                                                                   |
| **hrOutOfDatabaseSpace**             | Il database ha raggiunto la dimensione massima di 16 GB.                                                                              |
| **hrOutOfCursors**                   | Cursori di tabella.                                                                                                            |
| **hrOutOfBuffers**                   | Buffer di pagine del database.                                                                                                    |
| **hrTooManyIndexes**                 | Troppi indici.                                                                                                      |
| **hrTooManyKeys**                    | Il numero di colonne in un indice è eccessivo.                                                                                          |
| **hrRecordDeleted**                  | Il record è stato eliminato.                                                                                                     |
| **hrReadVerifyFailure**              | Si è verificato un errore di verifica di lettura.                                                                                              |
| **hrOutOfFileHandles**               | Handle di file esauriti.                                                                                                             |
| **hrDiskIO**                         | Si è verificato un errore di I/O su disco.                                                                                                       |
| **hrInvalidPath**                    | Il percorso del file non è valido.                                                                                                 |
| **hrRecordTooBig**                   | Il record ha superato le dimensioni massime.                                                                                        |
| **hrTooManyOpenDatabases**           | Troppi database aperti.                                                                                               |
| **hrInvalidDatabase**                | Il file non è un file di database.                                                                                                 |
| **hrNotInitialized**                 | Il database non è stato ancora chiamato.                                                                                                 |
| **hrAlreadyInitialized**             | Il database è già stato chiamato.                                                                                                 |
| **hrFileAccessDenied**               | Non è possibile accedere al file.                                                                                                       |
| **hrBufferTooSmall**                 | Il buffer è troppo piccolo.                                                                                                         |
| **hrSeekNotEqual**                   | SeekLE o SeekGE non è in grado di trovare una corrispondenza esatta.                                                                              |
| **hrTooManyColumns**                 | Troppe colonne definite.                                                                                              |
| **hrContainerNotEmpty**              | Il contenitore non è vuoto.                                                                                                      |
| **hrInvalidFilename**                | Il nome file non è valido.                                                                                                         |
| **hrInvalidBookmark**                | Il segnalibro non è valido.                                                                                                         |
| **hrColumnInUse**                    | La colonna viene utilizzata in un indice.                                                                                                  |
| **hrInvalidBufferSize**              | Il buffer di dati non corrisponde alle dimensioni della colonna.                                                                                  |
| **hrColumnNotUpdatable**             | Impossibile impostare il valore della colonna.                                                                                                  |
| **hrIndexInUse**                     | L'indice è in uso.                                                                                                             |
| **hrNullKeyDisallowed**              | Chiavi null non consentite in un indice.                                                                                           |
| **hrNotInTransaction**               | L'operazione deve essere all'interno di una transazione.                                                                                      |
| **hrNoIdleActivity**                 | Non è stata eseguita alcuna attività inattiva.                                                                                                       |
| **hrTooManyActiveUsers**             | Troppi utenti di database attivi.                                                                                        |
| **hrInvalidCountry**                 | Il codice paese o area geografica non è noto o non è valido.                                                                    |
| **hrInvalidLanguageId**              | L'ID lingua non è noto o non è valido.                                                                               |
| **hrInvalidCodePage**                | La tabella codici non è nota o non è valida.                                                                                 |
| **hrNoWriteLock**                    | Nessun blocco di scrittura a livello di transazione 0.                                                                                   |
| **hrColumnSetNull**                  | Il valore della colonna è impostato su null.                                                                                                 |
| **hrVersionStoreOutOfMemory**        | LMaxVerPages superato (solo XJET).                                                                                           |
| **hrCurrencyStackOutOfMemory**       | Cursori.                                                                                                                  |
| **hrOutOfSessions**                  | Sessioni inattive.                                                                                                                 |
| **hrWriteConflict**                  | Il blocco di scrittura non è riuscito a causa di un blocco di scrittura in attesa.                                                                          |
| **hrTransTooDeep**                   | Le transazioni sono annidate troppo profondamente.                                                                                          |
| **hrInvalidSesid**                   | Handle di sessione non valido.                                                                                                   |
| **hrSessionWriteConflict**           | Un'altra sessione dispone di una versione privata della pagina.                                                                               |
| **hrInTransaction**                  | Operazione non consentita all'interno di una transazione.                                                                               |
| **hrDatabaseDuplicate**              | Il database esiste già.                                                                                                     |
| **hrDatabaseInUse**                  | Il database è in uso.                                                                                                          |
| **hrDatabaseNotFound**               | Il database non esiste.                                                                                                     |
| **hrDatabaseInvalidName**            | Il nome del database non è valido.                                                                                                    |
| **hrDatabaseInvalidPages**           | Il numero di pagine non è valido.                                                                                                  |
| **hrDatabaseCorrupted**              | Il file di database è danneggiato o non è stato trovato.                                                                          |
| **hrDatabaseLocked**                 | Il database è bloccato.                                                                                                          |
| **hrTableEmpty**                     | È stata aperta una tabella vuota.                                                                                                       |
| **hrTableLocked**                    | La tabella è bloccata.                                                                                                             |
| **hrTableDuplicate**                 | La tabella esiste già.                                                                                                        |
| **hrTableInUse**                     | Impossibile bloccare la tabella perché è già in uso.                                                                           |
| **hrObjectNotFound**                 | La tabella o l'oggetto non esiste.                                                                                              |
| **hrCannotRename**                   | Impossibile rinominare il file temporaneo.                                                                                             |
| **hrDensityInvalid**                 | La densità di file/indici non è valida.                                                                                               |
| **hrTableNotEmpty**                  | Impossibile definire l'indice cluster.                                                                                            |
| **hrInvalidTableId**                 | ID di tabella non valido.                                                                                                         |
| **hrTooManyOpenTables**              | Non è possibile aprire altre tabelle.                                                                                                  |
| **hrIllegalOperation**               | L'operazione non è supportata nelle tabelle.                                                                                        |
| **hrObjectDuplicate**                | Il nome della tabella o dell'oggetto è già in uso.                                                                                  |
| **hrInvalidObject**                  | L'oggetto non è valido per l'operazione.                                                                                             |
| **hrIndexCantBuild**                 | Impossibile compilare un indice cluster.                                                                                               |
| **hrIndexHasPrimary**                | L'indice primario è già definito.                                                                                            |
| **hrIndexDuplicate**                 | L'indice è già definito.                                                                                                    |
| **hrIndexNotFound**                  | Indice inesistente.                                                                                                        |
| **hrIndexMustStay**                  | Impossibile eliminare un indice cluster.                                                                                              |
| **hrIndexInvalidDef**                | La definizione dell'indice non è valida.                                                                                                 |
| **hrIndexHasClustered**              | L'indice cluster è già definito.                                                                                          |
| **hrCreateIndexFailed**              | Impossibile creare l'indice perché si è verificato un errore durante la creazione di una tabella.                                                     |
| **hrTooManyOpenIndexes**             | Blocchi per la descrizione dell'indice.                                                                                                 |
| **hrColumnLong**                     | Il valore della colonna è troppo lungo.                                                                                                    |
| **hrColumnDoesNotFit**               | Il campo non rientrerà nel record.                                                                                            |
| **hrNullInvalid**                    | Il valore non può essere null.                                                                                                        |
| **hrColumnIndexed**                  | Non è possibile eliminare perché la colonna è indicizzata.                                                                                  |
| **hrColumnTooBig**                   | La lunghezza del campo supera la lunghezza massima consentita di 255 byte.                                                                 |
| **hrColumnNotFound**                 | Impossibile trovare la colonna.                                                                                                       |
| **hrColumnDuplicate**                | Il campo è già definito.                                                                                                    |
| **hrColumn2ndSysMaint**              | Per ogni tabella è consentito un solo incremento automatico o una sola colonna della versione.                                                                  |
| **hrInvalidColumnType**              | Il tipo di dati della colonna non è valido.                                                                                                 |
| **hrColumnMaxTruncated**             | La colonna è stata troncata perché supera la lunghezza massima consentita di 255 byte.                                                    |
| **hrColumnCannotIndex**              | Impossibile indicizzare una colonna di valori Long.                                                                                             |
| **hrTaggedNotNULL**                  | Le colonne con tag non possono essere null.                                                                                                   |
| **hrNoCurrentIndex**                 | La voce non è valida senza un indice corrente.                                                                                    |
| **hrKeyIsMade**                      | La chiave è stata completata.                                                                                                             |
| **hrBadColumnId**                    | ID di colonna non corretto.                                                                                                      |
| **hrBadItagSequence**                | È presente un identificatore di istanza non valido per una colonna multivalore.                                                                     |
| **hrCannotBeTagged**                 | L'incremento automatico e la versione non possono essere multivalore.                                                                                 |
| **hrRecordNotFound**                 | La chiave non è stata trovata.                                                                                                          |
| **hrNoCurrentRecord**                | La valuta non si trova in un record.                                                                                                 |
| **hrRecordClusteredChanged**         | Impossibile modificare una chiave cluster.                                                                                               |
| **hrKeyDuplicate**                   | La chiave esiste già.                                                                                                          |
| **hrAlreadyPrepared**                | La voce corrente è già stata copiata o cancellata.                                                                            |
| **hrKeyNotMade**                     | Non è stato creato alcun tasto.                                                                                                                 |
| **hrUpdateNotPrepared**              | Aggiornamento non preparato.                                                                                                         |
| **hrwrnDataHasChanged**              | I dati sono stati modificati.                                                                                                                |
| **hrerrDataHasChanged**              | L'operazione è stata abbandonata perché i dati sono stati modificati.                                                                            |
| **hrKeyChanged**                     | Spostato in una nuova chiave.                                                                                                              |
| **hrTooManySorts**                   | Troppi processi di ordinamento.                                                                                               |
| **hrInvalidOnSort**                  | Si è verificata un'operazione non valida nell'ordinamento.                                                                               |
| **hrTempFileOpenError**              | Non è possibile aprire il file temporaneo.                                                                                               |
| **hrTooManyAttachedDatabases**       | Troppi database aperti.                                                                                               |
| **hrDiskFull**                       | Disco pieno.                                                                                                                |
| **hrPermissionDenied**               | Autorizzazione negata.                                                                                                            |
| **hrFileNotFound**                   | Il file non è stato trovato.                                                                                                         |
| **hrFileOpenReadOnly**               | Il file di database è di sola lettura.                                                                                                  |
| **hrAfterInitialization**            | Impossibile eseguire il ripristino dopo l'inizializzazione.                                                                                          |
| **hrLogCorrupted**                   | I file di log del database sono danneggiati.                                                                                              |
| **hrInvalidOperation**               | Operazione non valida.                                                                                                        |
| **hrAccessDenied**                   | Accesso negato.                                                                                                                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Success](success.md)
</dt> <dt>

[Errori di backup in Active Directory Domain Services](backup-errors-in-active-directory-domain-services.md)
</dt> <dt>

[Errori di sistema in Active Directory Domain Services](system-errors-in-active-directory-domain-services.md)
</dt> <dt>

[Errori di Directory Manager](directory-manager-errors.md)
</dt> <dt>

[Valori restituiti per le funzioni in Active Directory Domain Services](return-values-for-functions-in-active-directory-domain-services.md)
</dt> </dl>

 

 




