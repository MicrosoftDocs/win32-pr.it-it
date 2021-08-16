---
title: Errori di registrazione e ripristino nelle funzioni in Active Directory Domain Services
description: In questo argomento vengono elencati i valori restituiti da errori di registrazione e ripristino per le funzioni in Active Directory Domain Services.
ms.assetid: b927073a-8bbc-45d4-b9d3-25f3aa6c6f53
ms.tgt_platform: multiple
keywords:
- Errori di registrazione e ripristino di Active Directory AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b267b359b5244fddc0e8a9b2ddfbfb5d6e5f9ab0a7e647683d44759f8a7261b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186592"
---
# <a name="logging-and-recovery-errors-in-functions-in-active-directory-domain-services"></a>Errori di registrazione e ripristino nelle funzioni in Active Directory Domain Services

In questo argomento vengono elencati i valori restituiti da errori di registrazione e ripristino per le funzioni in Active Directory Domain Services.



| Valore                                | Descrizione                                                                                                                      |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **hrLogFileCorrupt**                 | Il file di log è danneggiato.                                                                                                         |
| **hrNoBackupDirectory**              | Non è stata specificata alcuna directory di backup.                                                                                                   |
| **hrBackupDirectoryNotEmpty**        | La directory di backup non è vuota.                                                                                               |
| **hrBackupInProgress**               | Il backup è attivo.                                                                                                                |
| **hrMissingPreviousLogFile**         | Manca un file di log per il checkpoint.                                                                                        |
| **hrLogWriteFail**                   | Impossibile scrivere nel file di log.                                                                                                 |
| **hrBadLogVersion**                  | La versione del file di log non è compatibile con la versione del database Windows NT/Windows 2000 Directory Service (NTDS). |
| **hrInvalidLogSequence**             | Il timestamp nel log successivo non corrisponde a quello previsto.                                                                 |
| **hrLoggingDisabled**                | Il log non è attivo.                                                                                                           |
| **hrLogBufferTooSmall**              | Il buffer di log è troppo piccolo per essere recuperato.                                                                                     |
| **hrLogSequenceEnd**                 | È stato superato il numero massimo di file di log.                                                                               |
| **hrNoBackup**                       | Non è in corso alcun backup.                                                                                                  |
| **hrInvalidBackupSequence**          | La chiamata di backup non è in sequenza.                                                                                              |
| **hrBackupNotAllowedYet**            | Impossibile eseguire ora un backup.                                                                                                  |
| **hrDeleteBackupFileFail**           | Impossibile eliminare il file di backup.                                                                                                |
| **hrMakeBackupDirectoryFail**        | Impossibile creare una directory temporanea di backup.                                                                                     |
| **hrInvalidBackup**                  | Non è possibile eseguire un backup incrementale quando è abilitata la registrazione circolare.                                                      |
| **hrRecoveredWithErrors**            | Si sono verificati errori durante il processo di ripristino.                                                                               |
| **hrMissingLogFile**                 | Manca il file di registro corrente.                                                                                                 |
| **hrLogDiskFull**                    | Disco di registro pieno.                                                                                                            |
| **hrBadLogSignature**                | Un file di log è danneggiato.                                                                                                           |
| **hrBadDbSignature**                 | Un file di database è danneggiato.                                                                                                      |
| **hrBadCheckpointSignature**         | Un file del checkpoint è danneggiato.                                                                                                    |
| **hrCheckpointCorrupt**              | Un file del checkpoint non è stato trovato o è danneggiato.                                                                       |
| **hrDatabaseInconsistent**           | Il database è danneggiato.                                                                                                         |
| **hrConsistentTimeMismatch**         | Mancata corrispondenza nell'ora dell'ultima coerenza del database.                                                                      |
| **hrPatchFileMismatch**              | Il file di patch non viene generato da questo backup.                                                                                |
| **hrRestoreLogTooLow**               | Il numero di log iniziale è troppo basso per il ripristino.                                                                              |
| **hrRestoreLogTooHigh**              | Il numero di log iniziale è troppo elevato per il ripristino.                                                                             |
| **hrGivenLogFileHasBadSignature**    | Il file di log scaricato dal nastro è danneggiato.                                                                                |
| **hrGivenLogFileIsNotContiguous**    | Impossibile trovare un file di log obbligatorio dopo il download del nastro.                                                               |
| **hrMissingRestoreLogFiles**         | I dati non vengono ripristinati completamente perché alcuni file di log sono mancanti.                                                               |
| **hrExistingLogFileHasBadSignature** | Il file di log nel percorso del file di log è danneggiato.                                                                                    |
| **hrExistingLogFileIsNotContiguous** | Impossibile trovare un file di log obbligatorio nel percorso del file di log.                                                                        |
| **hrMissingFullBackup**              | Il database non ha eseguito un backup completo precedente prima del backup incrementale.                                                        |
| **hrBadBackupDatabaseSize**          | Le dimensioni del database di backup devono essere un multiplo di 4000 (4096 byte).                                                                |
| **hrTermInProgress**                 | È in corso l'arresto del database.                                                                                                 |
| **hrFeatureNotAvailable**            | La funzionalità non è disponibile.                                                                                                    |
| **hrInvalidName**                    | Il nome non è valido.                                                                                                             |
| **hrInvalidParameter**               | Il parametro non è valido.                                                                                                        |
| **hrColumnNull**                     | Il valore della colonna è Null.                                                                                                 |
| **hrBufferTruncated**                | Il buffer è troppo piccolo per i dati.                                                                                                |
| **hrDatabaseAttached**               | Il database è già collegato.                                                                                                |
| **hrInvalidDatabaseId**              | L'ID del database non è valido.                                                                                                      |
| **hrOutOfMemory**                    | La memoria del computer è insufficiente.                                                                                                   |
| **hrOutOfDatabaseSpace**             | Il database ha raggiunto le dimensioni massime di 16 GB.                                                                              |
| **hrOutOfCursors**                   | Cursori fuori tabella.                                                                                                            |
| **hrOutOfBuffers**                   | Buffer di pagina del database non in uscita.                                                                                                    |
| **hrTooManyIndexes**                 | Sono presenti troppi indici.                                                                                                      |
| **hrTooManyKeys**                    | Un indice contiene troppe colonne.                                                                                          |
| **hrRecordDeleted**                  | Il record è stato eliminato.                                                                                                     |
| **hrReadVerifyFailure**              | Si è verificato un errore di verifica di lettura.                                                                                              |
| **hrOutOfFileHandles**               | Handle di file esauriti.                                                                                                             |
| **hrDiskIO**                         | Si è verificato un errore di I/O su disco.                                                                                                       |
| **hrInvalidPath**                    | Il percorso del file non è valido.                                                                                                 |
| **hrRecordTooBig**                   | Il record ha superato le dimensioni massime.                                                                                        |
| **hrTooManyOpenDatabases**           | Sono presenti troppi database aperti.                                                                                               |
| **hrInvalidDatabase**                | Il file non è un file di database.                                                                                                 |
| **hrNotInitialized**                 | Il database non è stato ancora chiamato.                                                                                                 |
| **hrAlreadyInitialized**             | Il database è già stato chiamato.                                                                                                 |
| **hrFileAccessDenied**               | Impossibile accedere al file.                                                                                                       |
| **hrBufferTooSmall**                 | Il buffer è troppo piccolo.                                                                                                         |
| **hrSeekNotEqual**                   | SeekLE o SeekGE non è in grado di trovare una corrispondenza esatta.                                                                              |
| **hrTooManyColumns**                 | Sono state definite troppe colonne.                                                                                              |
| **hrContainerNotEmpty**              | Il contenitore non è vuoto.                                                                                                      |
| **hrInvalidFilename**                | Il nome file non è valido.                                                                                                         |
| **hrInvalidBookmark**                | Il segnalibro non è valido.                                                                                                         |
| **hrColumnInUse**                    | La colonna viene utilizzata in un indice.                                                                                                  |
| **hrInvalidBufferSize**              | Il buffer di dati non corrisponde alle dimensioni della colonna.                                                                                  |
| **hrColumnNotUpdatable**             | Impossibile impostare il valore della colonna.                                                                                                  |
| **hrIndexInUse**                     | L'indice è in uso.                                                                                                             |
| **hrNullKeyDisallowed**              | Le chiavi Null non sono consentite in un indice.                                                                                           |
| **hrNotInTransaction**               | L'operazione deve essere all'interno di una transazione.                                                                                      |
| **hrNoIdleActivity**                 | Non si è verificata alcuna attività inattiva.                                                                                                       |
| **hrTooManyActiveUsers**             | Sono presenti troppi utenti di database attivi.                                                                                        |
| **hrInvalidCountry**                 | Il codice paese o area geografica non è noto o non è valido.                                                                    |
| **hrInvalidLanguageId**              | L'ID lingua non è noto o non è valido.                                                                               |
| **hrInvalidCodePage**                | La tabella codici non è nota o non è valida.                                                                                 |
| **hrNoWriteLock**                    | Non esiste alcun blocco di scrittura a livello di transazione 0.                                                                                   |
| **hrColumnSetNull**                  | Il valore della colonna è impostato su Null.                                                                                                 |
| **hrVersionStoreOutOfMemory**        | Superamento di lMaxVerPages (solo XMAX).                                                                                           |
| **hrCurrencyStackOutOfMemory**       | Cursori non più in forma.                                                                                                                  |
| **hrOutOfSessions**                  | Sessioni non attive.                                                                                                                 |
| **hrWriteConflict**                  | Il blocco di scrittura non è riuscito a causa di un blocco di scrittura in sospeso.                                                                          |
| **hrTransTooDeep**                   | Le transazioni sono annidate troppo in profondità.                                                                                          |
| **hrInvalidSesid**                   | L'handle di sessione non è valido.                                                                                                   |
| **hrSessionWriteConflict**           | Un'altra sessione ha una versione privata della pagina.                                                                               |
| **hrInTransaction**                  | L'operazione non è consentita all'interno di una transazione.                                                                               |
| **hrDatabaseDuplicate**              | Il database esiste già.                                                                                                     |
| **hrDatabaseInUse**                  | Il database è in uso.                                                                                                          |
| **hrDatabaseNotFound**               | Il database non esiste.                                                                                                     |
| **hrDatabaseInvalidName**            | Il nome del database non è valido.                                                                                                    |
| **hrDatabaseInvalidPages**           | Il numero di pagine non è valido.                                                                                                  |
| **hrDatabaseCorrupted**              | Il file di database è danneggiato o non è possibile trovare.                                                                          |
| **hrDatabaseLocked**                 | Il database è bloccato.                                                                                                          |
| **hrTableEmpty**                     | È stata aperta una tabella vuota.                                                                                                       |
| **hrTableLocked**                    | La tabella è bloccata.                                                                                                             |
| **hrTableDuplicate**                 | La tabella esiste già.                                                                                                        |
| **hrTableInUse**                     | Impossibile bloccare la tabella perché è già in uso.                                                                           |
| **hrObjectNotFound**                 | La tabella o l'oggetto non esiste.                                                                                              |
| **hrCannotRename**                   | Impossibile rinominare il file temporaneo.                                                                                             |
| **hrDensityInvalid**                 | La densità di file/indice non è valida.                                                                                               |
| **hrTableNotEmpty**                  | Impossibile definire l'indice cluster.                                                                                            |
| **hrInvalidTableId**                 | L'ID tabella non è valido.                                                                                                         |
| **hrTooManyOpenTables**              | Impossibile aprire altre tabelle.                                                                                                  |
| **hrIllegalOperation**               | L'operazione non è supportata nelle tabelle.                                                                                        |
| **hrObjectDuplicate**                | Il nome della tabella o dell'oggetto è già in uso.                                                                                  |
| **hrInvalidObject**                  | L'oggetto non è valido per l'operazione.                                                                                             |
| **hrIndexIndexBuild**                 | Impossibile compilare un indice cluster.                                                                                               |
| **hrIndexHasPrimary**                | L'indice primario è già definito.                                                                                            |
| **hrIndexDuplicate**                 | L'indice è già definito.                                                                                                    |
| **hrIndexNotFound**                  | L'indice non esiste.                                                                                                        |
| **hrIndexMustStay**                  | Impossibile eliminare un indice cluster.                                                                                              |
| **hrIndexInvalidDef**                | La definizione dell'indice non è valida.                                                                                                 |
| **hrIndexHasClustered**              | L'indice cluster è già definito.                                                                                          |
| **hrCreateIndexFailed**              | Impossibile creare l'indice perché si è verificato un errore durante la creazione di una tabella.                                                     |
| **hrTooManyOpenIndexes**             | Blocchi di descrizione dell'indice non disponibili.                                                                                                 |
| **hrColumnLong**                     | Il valore della colonna è troppo lungo.                                                                                                    |
| **hrColumnDoesNotFit**               | Il campo non rientra nel record.                                                                                            |
| **hrNullInvalid**                    | Il valore non può essere null.                                                                                                        |
| **hrColumnIndexed**                  | Impossibile eliminare perché la colonna è indicizzata.                                                                                  |
| **hrColumnTooBig**                   | La lunghezza del campo supera la lunghezza massima di 255 byte.                                                                 |
| **hrColumnNotFound**                 | Impossibile trovare la colonna.                                                                                                       |
| **hrColumnDuplicate**                | Il campo è già definito.                                                                                                    |
| **hrColumn2ndSysMaint**              | È consentita una sola colonna con incremento automatico o versione per tabella.                                                                  |
| **hrInvalidColumnType**              | Il tipo di dati della colonna non è valido.                                                                                                 |
| **hrColumnMaxTruncated**             | La colonna è stata troncata perché ha superato la lunghezza massima di 255 byte.                                                    |
| **hrColumnCannotIndex**              | Impossibile indicizzare una colonna con valori long.                                                                                             |
| **hrTaggedNotNULL**                  | Le colonne con tag non possono essere Null.                                                                                                   |
| **hrNoCurrentIndex**                 | La voce non è valida senza un indice corrente.                                                                                    |
| **hrKeyIs Made**                      | La chiave è completa.                                                                                                             |
| **hrBadColumnId**                    | L'ID di colonna non è corretto.                                                                                                      |
| **hrBadItagSequence**                | Identificatore di istanza non valido per una colonna multivalore.                                                                     |
| **hrCannotBeTagged**                 | AutoIncrement e Version non possono essere multivalore.                                                                                 |
| **hrRecordNotFound**                 | Impossibile trovare la chiave.                                                                                                          |
| **hrNoCurrentRecord**                | La valuta non è in un record.                                                                                                 |
| **hrRecordClusteredChanged**         | Non è possibile modificare una chiave cluster.                                                                                               |
| **hrKeyDuplicate**                   | La chiave esiste già.                                                                                                          |
| **hrAlreadyPrepared**                | La voce corrente è già stata copiata o cancellata.                                                                            |
| **hrKeyNotNotNot**                     | Non è stata effettuata alcuna chiave.                                                                                                                 |
| **hrUpdateNotPrepared**              | L'aggiornamento non è stato preparato.                                                                                                         |
| **hrwrnDataHasChanged**              | I dati sono stati modificati.                                                                                                                |
| **hrerrDataHasChanged**              | L'operazione è stata abbandonata perché i dati sono stati modificati.                                                                            |
| **hrKeyChanged**                     | Spostato in una nuova chiave.                                                                                                              |
| **hrTooManySorts**                   | Sono presenti troppi processi di ordinamento.                                                                                               |
| **hrInvalidOnSort**                  | Operazione non valida nell'ordinamento.                                                                               |
| **hrTempFileOpenError**              | Impossibile aprire il file temporaneo.                                                                                               |
| **hrTooManyAttachedDatabases**       | Troppi database aperti.                                                                                               |
| **hrDiskFull**                       | Disco pieno.                                                                                                                |
| **hrPermissionDenied**               | Autorizzazione negata.                                                                                                            |
| **hrFileNotFound**                   | Impossibile trovare il file.                                                                                                         |
| **hrFileOpenReadOnly**               | Il file di database è di sola lettura.                                                                                                  |
| **hrAfterInitialization**            | Impossibile eseguire il ripristino dopo l'inizializzazione.                                                                                          |
| **hrLogCorrupted**                   | I file di log del database sono danneggiati.                                                                                              |
| **hrInvalidOperation**               | L'operazione non è valida.                                                                                                        |
| **hrAccessDenied**                   | Accesso negato.                                                                                                                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Success](success.md)
</dt> <dt>

[Errori di backup in Active Directory Domain Services](backup-errors-in-active-directory-domain-services.md)
</dt> <dt>

[Errori di sistema in Active Directory Domain Services](system-errors-in-active-directory-domain-services.md)
</dt> <dt>

[Errori di Gestione directory](directory-manager-errors.md)
</dt> <dt>

[Valori restituiti per le funzioni in Active Directory Domain Services](return-values-for-functions-in-active-directory-domain-services.md)
</dt> </dl>

 

 




