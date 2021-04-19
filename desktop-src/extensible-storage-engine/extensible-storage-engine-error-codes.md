---
description: 'Altre informazioni su: codici di errore Extensible Storage Engine'
title: Codici di errore di Extensible Storage Engine
TOCTitle: Extensible Storage Engine Error Codes
ms:assetid: 7534370d-aed6-4980-b1ca-c3d063507e31
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269297(v=EXCHG.10)
ms:contentKeyID: 32765589
ms.date: 09/22/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9de4bd8157e0b7210315352ba0760293a892f087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317417"
---
# <a name="extensible-storage-engine-error-codes"></a>Codici di errore di Extensible Storage Engine


_**Si applica a:** Windows | Windows Server_

## <a name="extensible-storage-engine-error-codes"></a>Codici di errore di Extensible Storage Engine

I codici di errore (flag) seguenti vengono usati dalle funzioni nell'API del motore di archiviazione estendibile.

Un [JET_ERR](./jet-err.md) valore pari a zero deve essere interpretato come operazione riuscita.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Operazione riuscita</p></th>
<th><p>Descrizione</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess 0</p></td>
<td><p>Funzione completata.</p></td>
</tr>
</tbody>
</table>


Un valore [JET_ERR](./jet-err.md) maggiore di zero deve essere interpretato come un avviso.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Avvisi</p></th>
<th><p>Descrizione</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_wrnRemainingVersions<br />
321</p></td>
<td><p>L'archivio versione è ancora attivo. Questo errore viene restituito da gestione directory.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnUniqueKey<br />
345</p></td>
<td><p>Una ricerca in un indice non univoco ha restituito una chiave univoca. Questo errore viene restituito da gestione directory.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnSeparateLongValue<br />
406</p></td>
<td><p>Una colonna di database è un valore Long separato. Questo errore viene restituito da Gestione record.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnExistingLogFileHasBadSignature<br />
558</p></td>
<td><p>Firma non valida per il file di log esistente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnExistingLogFileIsNotContiguous<br />
559</p></td>
<td><p>Il file di log esistente non è contiguo.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnSkipThisRecord<br />
564</p></td>
<td><p>Questo errore è solo per uso interno.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnTargetInstanceRunning<br />
578</p></td>
<td><p>Il TargetInstance specificato per il ripristino è in esecuzione.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDatabaseRepaired<br />
595</p></td>
<td><p>Il danneggiamento del database è stato ripristinato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnNull<br />
1004</p></td>
<td><p>Il valore della colonna è <strong>null</strong> .</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnBufferTruncated<br />
1006</p></td>
<td><p>Il buffer è troppo piccolo per i dati.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnDatabaseAttached<br />
1007</p></td>
<td><p>Il database è già collegato.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnSortOverflow<br />
1009</p></td>
<td><p>L'ordinamento che si sta tentando non dispone di memoria sufficiente per il completamento.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnSeekNotEqual<br />
1039</p></td>
<td><p>Non è stata trovata una corrispondenza esatta durante una ricerca.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnRecordFoundGreater<br />
JET_wrnSeekNotEqual</p></td>
<td><p>Non è stata trovata una corrispondenza esatta durante una ricerca. Questo errore viene restituito da Gestione record.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnRecordFoundLess<br />
JET_wrnSeekNotEqual</p></td>
<td><p>Non è stata trovata una corrispondenza esatta durante una ricerca. Questo errore viene restituito da Gestione record.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnNoErrorInfo<br />
1055</p></td>
<td><p>Non sono presenti informazioni estese sull'errore.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnNoIdleActivity<br />
1058</p></td>
<td><p>Non è stata eseguita alcuna attività inattiva.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnNoWriteLock<br />
1067</p></td>
<td><p>Non esiste un blocco di scrittura a livello di transazione 0.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnSetNull<br />
1068</p></td>
<td><p>La colonna è impostata su un valore <strong>null</strong> .</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnTableEmpty<br />
1301</p></td>
<td><p>È stata aperta una tabella vuota.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnTableInUseBySystem<br />
1327</p></td>
<td><p>Per la pulizia del sistema è presente un cursore aperto sulla tabella.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnCorruptIndexDeleted<br />
1415</p></td>
<td><p>L'indice non aggiornato deve essere rimosso.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMaxTruncated<br />
1512</p></td>
<td><p>La lunghezza massima è troppo grande ed è stata troncata.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnCopyLongValue<br />
1520</p></td>
<td><p>Un valore BLOB è stato spostato dal record in una risorsa di archiviazione separata di BLOB di grandi dimensioni.</p>
<p><strong>Nota</strong> Questo errore è solo per uso interno.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnSkipped<br />
1531</p></td>
<td><p>I valori della colonna non sono stati restituiti perché l'ID di colonna o il membro <em>itagSequence</em> corrispondente della struttura <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a> richiesta per l'enumerazione è null.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnNotLocal<br />
1532</p></td>
<td><p>I valori della colonna non sono stati restituiti perché non è stato possibile ricostruire i dati esistenti.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMoreTags<br />
1533</p></td>
<td><p>I valori di colonna esistenti non sono stati richiesti per l'enumerazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnTruncated<br />
1534</p></td>
<td><p>Il valore della colonna è stato troncato al limite delle dimensioni richiesto durante l'enumerazione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnPresent<br />
1535</p></td>
<td><p>I valori della colonna esistono ma non sono stati restituiti dalla richiesta.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnSingleValue<br />
1536</p></td>
<td><p>Il valore della colonna è stato restituito in JET_COLUMNENUM come risultato della JET_bitEnumerateCompressOutput da impostare.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnDefault<br />
1537</p></td>
<td><p>Il valore della colonna viene impostato sul valore predefinito della colonna.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDataHasChanged<br />
1610</p></td>
<td><p>I dati sono stati modificati.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnKeyChanged<br />
1618</p></td>
<td><p>Viene utilizzata una nuova chiave.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnFileOpenReadOnly<br />
1813</p></td>
<td><p>Il file di database è di sola lettura.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnIdleFull<br />
1908</p></td>
<td><p>Il registro di sistema inattivo è pieno.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDefragAlreadyRunning<br />
2000</p></td>
<td><p>Una deframmentazione in linea è già in esecuzione nel database specificato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnDefragNotRunning<br />
2001</p></td>
<td><p>Una deframmentazione in linea non è in esecuzione nel database specificato.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnCallbackNotRegistered<br />
2100</p></td>
<td><p>È stata annullata la registrazione di una funzione di callback non esistente.</p></td>
</tr>
</tbody>
</table>


Un [JET_ERR](./jet-err.md) valore minore di zero deve essere interpretato come un errore.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Errors</p></th>
<th><p>Descrizione</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_wrnNyi<br />
-1</p></td>
<td><p>La funzione non è ancora implementata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRfsFailure<br />
-100</p></td>
<td><p>Il simulatore di errore delle risorse non è riuscito.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRfsNotArmed<br />
-101</p></td>
<td><p>Il simulatore di errore delle risorse non è stato inizializzato.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileClose<br />
-102</p></td>
<td><p>Non è stato possibile chiudere il file.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfThreads<br />
-103</p></td>
<td><p>Impossibile avviare il thread.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyIO<br />
-105</p></td>
<td><p>Il sistema è occupato a causa di un numero eccessivo di IOs.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTaskDropped<br />
-106</p></td>
<td><p>Non è stato possibile eseguire l'attività asincrona richiesta.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInternalError<br />
-107</p></td>
<td><p>Si è verificato un errore interno irreversibile.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseBufferDependenciesCorrupted<br />
-255</p></td>
<td><p>Le dipendenze del buffer sono state impostate in modo errato e si è verificato un errore di ripristino.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPreviousVersion<br />
-322</p></td>
<td><p>La versione esisteva già e si è verificato un errore di ripristino. Questo errore viene restituito da gestione directory.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPageBoundary<br />
-323</p></td>
<td><p>È stato raggiunto il limite della pagina. Questo errore viene restituito da gestione directory.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyBoundary<br />
-324</p></td>
<td><p>È stato raggiunto il limite della chiave. Questo errore viene restituito da gestione directory.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadPageLink<br />
-327</p></td>
<td><p>Il database è danneggiato. Questo errore viene restituito da gestione directory.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadBookmark<br />
-328</p></td>
<td><p>Il segnalibro non ha alcun indirizzo corrispondente nel database. Questo errore viene restituito da gestione directory.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNTSystemCallFailed<br />
-334</p></td>
<td><p>La chiamata al sistema operativo non è riuscita. Questo errore viene restituito da gestione directory.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadParentPageLink<br />
-338</p></td>
<td><p>Un database padre è danneggiato. Questo errore viene restituito da gestione directory.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSPAvailExtCacheOutOfSync<br />
-340</p></td>
<td><p>La cache AvailExt non corrisponde all'albero B +. Questo errore viene restituito da gestione directory.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSPAvailExtCorrupted<br />
-341</p></td>
<td><p>L'albero dello spazio AllAvailExt è danneggiato. Questo errore viene restituito da gestione directory.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSPAvailExtCacheOutOfMemory<br />
-342</p></td>
<td><p>Si è verificato un errore di memoria insufficiente durante l'allocazione di un nodo della cache AvailExt. Questo errore viene restituito da gestione directory.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSPOwnExtCorrupted<br />
-343</p></td>
<td><p>L'albero dello spazio OwnExt è danneggiato. Questo errore viene restituito da gestione directory.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDbTimeCorrupted<br />
-344</p></td>
<td><p>Dbtime nella pagina corrente è maggiore del valore di dbtime del database globale. Questo errore viene restituito da gestione directory.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyTruncated<br />
-346</p></td>
<td><p>Il tentativo di creare una chiave per una voce di indice non è riuscito perché la chiave sarebbe stata troncata e la definizione dell'indice non consentiva il troncamento della chiave.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyTooBig<br />
-408</p></td>
<td><p>Chiave troppo grande. Questo errore viene restituito da Gestione record.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLoggedOperation<br />
-500</p></td>
<td><p>Impossibile ripetere l'operazione registrata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogFileCorrupt<br />
-501</p></td>
<td><p>Il file di log è danneggiato.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackupDirectory<br />
-503</p></td>
<td><p>Non è stata specificata una directory di backup.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBackupDirectoryNotEmpty<br />
-504</p></td>
<td><p>La directory di backup non è vuota.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupInProgress<br />
-505</p></td>
<td><p>Il backup è già attivo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress<br />
-506</p></td>
<td><p>È in corso un ripristino.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingPreviousLogFile<br />
-509</p></td>
<td><p>Il file di log non è presente per il punto di controllo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogWriteFail<br />
-510</p></td>
<td><p>Si è verificato un errore durante la scrittura nel file di log.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogDisabledDueToRecoveryFailure<br />
-511</p></td>
<td><p>Il tentativo di scrittura nel log dopo il ripristino non è riuscito.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotLogDuringRecoveryRedo<br />
-512</p></td>
<td><p>Tentativo di scrittura nel log durante il ripristino del ripristino non riuscito.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogGenerationMismatch<br />
-513</p></td>
<td><p>Il nome del file di log non corrisponde al numero di generazione interno.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadLogVersion<br />
-514</p></td>
<td><p>La versione del file di registro non è compatibile con la versione ESE.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLogSequence<br />
-515</p></td>
<td><p>Il timestamp nel log successivo non corrisponde al timestamp previsto.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLoggingDisabled<br />
-516</p></td>
<td><p>Il log non è attivo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogBufferTooSmall<br />
-517</p></td>
<td><p>Il buffer del log è troppo piccolo per il ripristino.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogSequenceEnd<br />
-519</p></td>
<td><p>È stato superato il numero massimo di file di log.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackup<br />
-520</p></td>
<td><p>Nessun backup in corso.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackupSequence<br />
-521</p></td>
<td><p>La chiamata di backup è fuori sequenza.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupNotAllowedYet<br />
-523</p></td>
<td><p>Non è possibile eseguire un backup in questo momento.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDeleteBackupFileFail<br />
-524</p></td>
<td><p>Non è stato possibile eliminare un file di backup.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMakeBackupDirectoryFail<br />
-525</p></td>
<td><p>Non è stato possibile creare la directory temporanea di backup.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackup<br />
-526</p></td>
<td><p>Registrazione circolare abilitata; non è possibile eseguire un backup incrementale.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecoveredWithErrors<br />
-527</p></td>
<td><p>I dati sono stati ripristinati con errori.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingLogFile<br />
-528</p></td>
<td><p>Manca il file di registro corrente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogDiskFull<br />
-529</p></td>
<td><p>Disco di registro pieno.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadLogSignature<br />
-530</p></td>
<td><p>Firma non valida per un file di log.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadDbSignature<br />
-531</p></td>
<td><p>Firma non valida per un file di database.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadCheckpointSignature<br />
-532</p></td>
<td><p>Firma non valida per un file del checkpoint.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCheckpointCorrupt<br />
-533</p></td>
<td><p>Il file del checkpoint non è stato trovato o è danneggiato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingPatchPage<br />
-534</p></td>
<td><p>Impossibile trovare la pagina file della patch del database durante il ripristino.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadPatchPage<br />
-535</p></td>
<td><p>La pagina del file di patch del database non è valida.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRedoAbruptEnded<br />
-536</p></td>
<td><p>Il rollforward si è improvvisamente interrotto a causa di un errore improvviso durante la lettura dei log dal file di log.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadSLVSignature<br />
-537</p></td>
<td><p>Questo flag è riservato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPatchFileMissing<br />
-538</p></td>
<td><p>Il ripristino hardware ha rilevato che nel set di backup manca un file di patch del database.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseLogSetMismatch<br />
-539</p></td>
<td><p>Il database non appartiene al set di file di log corrente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseStreamingFileMismatch<br />
-540</p></td>
<td><p>Questo flag è riservato.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogFileSizeMismatch<br />
-541</p></td>
<td><p>Le dimensioni effettive del file di log non corrispondono <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCheckpointFileNotFound<br />
-542</p></td>
<td><p>Impossibile trovare il file del checkpoint.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRequiredLogFilesMissing<br />
-543</p></td>
<td><p>Mancano i file di log necessari per il ripristino.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSoftRecoveryOnBackupDatabase<br />
-544</p></td>
<td><p>Un ripristino soft sta per essere utilizzato in un database di backup quando è necessario utilizzare un ripristino.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogFileSizeMismatchDatabasesConsistent<br />
-545</p></td>
<td><p>I database sono stati ripristinati, ma le dimensioni del file di log utilizzate durante il ripristino non corrispondono <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogSectorSizeMismatch<br />
-546</p></td>
<td><p>Le dimensioni del settore del file di log non corrispondono a quelle del volume corrente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogSectorSizeMismatchDatabasesConsistent<br />
-547</p></td>
<td><p>I database sono stati ripristinati, ma le dimensioni del settore del file di log (usate durante il ripristino) non corrispondono alle dimensioni del settore del volume corrente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogSequenceEndDatabasesConsistent<br />
-548</p></td>
<td><p>I database sono stati ripristinati, ma sono state usate tutte le generazioni di log possibili nella sequenza corrente. Prima di continuare, è necessario eliminare tutti i file di registro e il file del checkpoint e il backup dei database.</p></td>
</tr>
<tr class="even">
<td><p>JET_errStreamingDataNotLogged<br />
-549</p></td>
<td><p>Si è verificato un tentativo non valido di riprodurre un'operazione di streaming di file in cui i dati non sono stati registrati. Questo è probabilmente causato da un tentativo di rollforward con la registrazione circolare abilitata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseDirtyShutdown<br />
-550</p></td>
<td><p>Il database non è stato arrestato in modo corretto. È innanzitutto necessario eseguire un ripristino per completare correttamente le operazioni di database per l'arresto precedente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInconsistent<br />
JET_errDatabaseDirtyShutdown</p></td>
<td><p>Questo errore è obsoleto ed è stato sostituito da JET_errDatabaseDirtyShutdown.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errConsistentTimeMismatch<br />
-551</p></td>
<td><p>Non è stata confrontata l'ora dell'ultimo coerente per il database.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabasePatchFileMismatch<br />
-552</p></td>
<td><p>Il file di patch del database non viene generato da questo backup.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errEndingRestoreLogTooLow<br />
-553</p></td>
<td><p>Il numero di log iniziale è troppo basso per il ripristino.</p></td>
</tr>
<tr class="even">
<td><p>JET_errStartingRestoreLogTooHigh<br />
-554</p></td>
<td><p>Il numero di log iniziale è troppo elevato per il ripristino.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errGivenLogFileHasBadSignature<br />
-555</p></td>
<td><p>La firma del file di log di ripristino non è valida.</p></td>
</tr>
<tr class="even">
<td><p>JET_errGivenLogFileIsNotContiguous<br />
-556</p></td>
<td><p>Il file di log di ripristino non è contiguo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingRestoreLogFiles<br />
-557</p></td>
<td><p>Alcuni file di log di ripristino risultano mancanti.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingFullBackup<br />
-560</p></td>
<td><p>Il database ha perso un backup completo precedente prima di provare a eseguire un backup incrementale.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadBackupDatabaseSize<br />
-561</p></td>
<td><p>Le dimensioni del database di backup non sono un multiplo delle dimensioni della pagina del database.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseAlreadyUpgraded<br />
-562</p></td>
<td><p>Il tentativo corrente di aggiornare un database è stato interrotto perché il database è già aggiornato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseIncompleteUpgrade<br />
-563</p></td>
<td><p>Il database è stato convertito solo parzialmente nel formato corrente. È necessario ripristinare il database dal backup.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingCurrentLogFiles<br />
-565</p></td>
<td><p>Alcuni file di registro correnti risultano mancanti per il ripristino continuo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDbTimeTooOld<br />
-566</p></td>
<td><p>Il valore di dbtime in una pagina è inferiore a quello di dbtimeBefore nel record.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDbTimeTooNew<br />
-567</p></td>
<td><p>Il dbtime in una pagina è in anticipo di dbtimeBefore nel record.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingFileToBackup<br />
-569</p></td>
<td><p>Alcuni file di patch del database o di log mancanti durante il backup.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogTornWriteDuringHardRestore<br />
-570</p></td>
<td><p>È stata rilevata una scrittura incompleta in un backup impostato durante un ripristino a freddo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogTornWriteDuringHardRecovery<br />
-571</p></td>
<td><p>È stata rilevata una scrittura incompleta durante un ripristino rigido (il log non faceva parte di un set di backup).</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogCorruptDuringHardRestore<br />
-573</p></td>
<td><p>Il danneggiamento è stato rilevato in un set di backup durante un ripristino a freddo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogCorruptDuringHardRecovery<br />
-574</p></td>
<td><p>Il danneggiamento è stato rilevato durante il ripristino rigido (il log non faceva parte di un set di backup).</p></td>
</tr>
<tr class="even">
<td><p>JET_errMustDisableLoggingForDbUpgrade<br />
-575</p></td>
<td><p>Non è possibile abilitare la registrazione durante il tentativo di aggiornamento di un database.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadRestoreTargetInstance<br />
-577</p></td>
<td><p>Il TargetInstance specificato per il ripristino non è stato trovato o i file di log non corrispondono.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecoveredWithoutUndo<br />
-579</p></td>
<td><p>Il motore di database ha rieseguito correttamente tutte le operazioni nel log delle transazioni per eseguire un ripristino di arresto anomalo, ma il chiamante ha scelto di arrestare il ripristino senza eseguire il rollback degli aggiornamenti non sottoposti a commit.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabasesNotFromSameSnapshot<br />
-580</p></td>
<td><p>I database da ripristinare non appartengono allo stesso backup della copia shadow.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSoftRecoveryOnSnapshot<br />
-581</p></td>
<td><p>Il ripristino di un database da un set di backup di copie shadow prevede un ripristino soft.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeTranslationBufferTooSmall<br />
-601</p></td>
<td><p>Il buffer della traduzione Unicode è troppo piccolo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errUnicodeTranslationFail<br />
-602</p></td>
<td><p>La normalizzazione Unicode non è riuscita.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeNormalizationNotSupported<br />
-603</p></td>
<td><p>Il sistema operativo non fornisce il supporto per la normalizzazione Unicode e non è stato specificato un callback di normalizzazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errExistingLogFileHasBadSignature<br />
-610</p></td>
<td><p>Firma non valida per il file di log esistente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errExistingLogFileIsNotContiguous<br />
-611</p></td>
<td><p>Un file di log esistente non è contiguo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogReadVerifyFailure<br />
-612</p></td>
<td><p>Si è verificato un errore di checksum nel file di log durante il backup.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSLVReadVerifyFailure<br />
-613</p></td>
<td><p>Questo flag è riservato.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCheckpointDepthTooDeep<br />
-614</p></td>
<td><p>Troppe generazioni in attesa tra il checkpoint e la generazione corrente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreOfNonBackupDatabase<br />
-615</p></td>
<td><p>Si è tentato di eseguire un ripristino rigido in un database che non era un database di backup.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidGrbit<br />
-900</p></td>
<td><p>Parametro grbit non valido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress<br />
-1000</p></td>
<td><p>Terminazione in corso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFeatureNotAvailable<br />
-1001</p></td>
<td><p>Questo elemento API non è supportato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidName<br />
-1002</p></td>
<td><p>È in uso un nome non valido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter<br />
-1003</p></td>
<td><p>Viene usato un parametro API non valido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseFileReadOnly<br />
-1008</p></td>
<td><p>Tentativo di connessione a un file di database di sola lettura per operazioni di lettura/scrittura.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabaseId<br />
-1010</p></td>
<td><p>ID database non valido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory<br />
-1011</p></td>
<td><p>Memoria insufficiente nel sistema.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfDatabaseSpace<br />
-1012</p></td>
<td><p>È stata raggiunta la dimensione massima del database.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfCursors<br />
-1013</p></td>
<td><p>La tabella non è presente nei cursori.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfBuffers<br />
-1014</p></td>
<td><p>Il database è esterno ai buffer di pagina.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyIndexes<br />
-1015</p></td>
<td><p>Troppi indici.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyKeys<br />
-1016</p></td>
<td><p>Il numero di colonne in un indice è eccessivo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordDeleted<br />
-1017</p></td>
<td><p>Il record è stato eliminato.</p></td>
</tr>
<tr class="even">
<td><p>JET_errReadVerifyFailure<br />
-1018</p></td>
<td><p>Si è verificato un errore di checksum in una pagina del database.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPageNotInitialized<br />
-1019</p></td>
<td><p>È presente una pagina di database vuota.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfFileHandles<br />
-1020</p></td>
<td><p>Nessun handle di file.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDiskIO<br />
-1022</p></td>
<td><p>Si è verificato un errore di i/o del disco.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPath<br />
-1023</p></td>
<td><p>Percorso di file non valido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidSystemPath<br />
-1024</p></td>
<td><p>Il percorso di sistema non è valido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLogDirectory<br />
-1025</p></td>
<td><p>Directory log non valida.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordTooBig<br />
-1026</p></td>
<td><p>Il record è più grande della dimensione massima.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenDatabases<br />
-1027</p></td>
<td><p>Troppi database aperti.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidDatabase<br />
-1028</p></td>
<td><p>Non si tratta di un file di database.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized<br />
-1029</p></td>
<td><p>Il motore di database non è stato inizializzato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errAlreadyInitialized<br />
-1030</p></td>
<td><p>Il motore di database è già inizializzato.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInitInProgress<br />
-1031</p></td>
<td><p>È in corso l'inizializzazione del motore di database.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileAccessDenied<br />
-1032</p></td>
<td><p>Non è possibile accedere al file perché il file è bloccato o in uso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBufferTooSmall<br />
-1038</p></td>
<td><p>Il buffer è troppo piccolo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyColumns<br />
-1040</p></td>
<td><p>Sono state definite troppe colonne.</p></td>
</tr>
<tr class="even">
<td><p>JET_errContainerNotEmpty<br />
-1043</p></td>
<td><p>Il contenitore non è vuoto.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidFilename<br />
-1044</p></td>
<td><p>Il nome file non è valido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBookmark<br />
-1045</p></td>
<td><p>Segnalibro non valido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnInUse<br />
-1046</p></td>
<td><p>La colonna utilizzata si trova in un indice.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize<br />
-1047</p></td>
<td><p>Il buffer di dati non corrisponde alle dimensioni della colonna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotUpdatable<br />
-1048</p></td>
<td><p>Impossibile impostare il valore della colonna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInUse<br />
-1051</p></td>
<td><p>L'indice è in uso.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLinkNotSupported<br />
-1052</p></td>
<td><p>Il supporto del collegamento non è disponibile.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNullKeyDisallowed<br />
-1053</p></td>
<td><p>Chiavi null non consentite in un indice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInTransaction<br />
-1054</p></td>
<td><p>L'operazione deve essere eseguita all'interno di una transazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyActiveUsers<br />
-1059</p></td>
<td><p>Troppi utenti di database attivi</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCountry<br />
-1061</p></td>
<td><p>È presente un codice paese non valido o sconosciuto.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId<br />
-1062</p></td>
<td><p>ID lingua non valido o sconosciuto.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCodePage<br />
-1063</p></td>
<td><p>Tabella codici non valida o sconosciuta.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLCMapStringFlags<br />
-1064</p></td>
<td><p>Flag non validi utilizzati per <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errVersionStoreEntryTooBig<br />
-1065</p></td>
<td><p>Si è tentato di creare una voce dell'archivio versioni (RCE) più grande di un bucket di versione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemoryAndCleanupTimedOut<br />
-1066</p></td>
<td><p>Memoria esaurita per l'archivio versioni. Impossibile completare il tentativo di pulizia.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errVersionStoreOutOfMemory<br />
-1069</p></td>
<td><p>Memoria insufficiente nell'archivio versioni ed è già stato effettuato un tentativo di pulizia.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotIndex<br />
-1071</p></td>
<td><p>Non è possibile indicizzare le colonne escrow e SLV.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordNotDeleted<br />
-1072</p></td>
<td><p>Il record non è stato eliminato.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyMempoolEntries<br />
-1073</p></td>
<td><p>Sono state richieste troppe voci mempool.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfObjectIDs<br />
-1074</p></td>
<td><p>Il database non è presente nell'albero B + ObjectID, quindi è necessario eseguire una deframmentazione non in linea per recuperare ObjectID liberati o non usati.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfLongValueIDs<br />
-1075</p></td>
<td><p>Il contatore ID valore Long ha raggiunto il valore massimo. È necessario eseguire una deframmentazione non in linea per recuperare la LongValueIDs gratuita o inutilizzata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfAutoincrementValues<br />
-1076</p></td>
<td><p>Il contatore di incremento automatico ha raggiunto il valore massimo. Una deframmentazione non in linea non sarà in grado di recuperare i valori di incremento automatico gratuiti o non usati.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfDbtimeValues<br />
-1077</p></td>
<td><p>Il contatore dbtime ha raggiunto il valore massimo. È necessario eseguire una deframmentazione non in linea per recuperare i valori dbtime liberi o inutilizzati.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfSequentialIndexValues<br />
-1078</p></td>
<td><p>Un contatore di indice sequenziale ha raggiunto il valore massimo. È necessario eseguire una deframmentazione non in linea per recuperare i valori SequentialIndex liberi o inutilizzati.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode<br />
-1080</p></td>
<td><p>Questa chiamata a istanze diverse ha la modalità a istanza singola abilitata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode<br />
-1081</p></td>
<td><p>Per questa chiamata a istanza singola è abilitata la modalità a istanze diverse.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSystemParamsAlreadySet<br />
-1082</p></td>
<td><p>I parametri di sistema globali sono già stati impostati.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSystemPathInUse<br />
-1083</p></td>
<td><p>Il percorso di sistema è già in uso da un'altra istanza del database.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogFilePathInUse<br />
-1084</p></td>
<td><p>Il percorso del file di log è già in uso da un'altra istanza del database.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTempPathInUse<br />
-1085</p></td>
<td><p>Il percorso del database temporaneo è già in uso da un'altra istanza di database.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceNameInUse<br />
-1086</p></td>
<td><p>Il nome dell'istanza è già in uso.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable<br />
-1090</p></td>
<td><p>Impossibile utilizzare questa istanza perché si è verificato un errore irreversibile.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseUnavailable<br />
-1091</p></td>
<td><p>Impossibile utilizzare il database perché si è verificato un errore irreversibile.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailableDueToFatalLogDiskFull<br />
-1092</p></td>
<td><p>Non è possibile usare questa istanza perché si è verificato un errore di log-Disk-Full durante l'esecuzione di un'operazione, ad esempio un rollback di transazione, che non è in grado di tollerare l'errore.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfSessions<br />
-1101</p></td>
<td><p>Il database non è presente nelle sessioni.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict<br />
-1102</p></td>
<td><p>Il blocco di scrittura non è riuscito a causa dell'esistenza di un blocco di scrittura in attesa.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransTooDeep<br />
-1103</p></td>
<td><p>Le transazioni sono annidate troppo profondamente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidSesid<br />
-1104</p></td>
<td><p>Handle di sessione non valido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errWriteConflictPrimaryIndex<br />
-1105</p></td>
<td><p>Si è tentato di eseguire un aggiornamento su un indice primario non sottoposta a commit.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction<br />
-1108</p></td>
<td><p>Operazione non consentita all'interno di una transazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRollbackRequired<br />
-1109</p></td>
<td><p>È necessario eseguire il rollback della transazione corrente. Non è possibile eseguire il commit e non è possibile avviarne uno nuovo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTransReadOnly<br />
-1110</p></td>
<td><p>Una transazione di sola lettura ha tentato di modificare il database.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionWriteConflict<br />
-1111</p></td>
<td><p>Si è tentato di sostituire lo stesso record con due cursori diversi nella stessa sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordTooBigForBackwardCompatibility<br />
-1112</p></td>
<td><p>Il record sarebbe troppo grande se rappresentato in un formato di database da una versione precedente di Jet.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotMaterializeForwardOnlySort<br />
-1113</p></td>
<td><p>Non è stato possibile creare la tabella temporanea a causa di parametri che sono in conflitto con JET_bitTTForwardOnly.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSesidTableIdMismatch<br />
-1114</p></td>
<td><p>Non è possibile usare l'handle di sessione con l'ID tabella perché non è stato usato per crearlo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidInstance<br />
-1115</p></td>
<td><p>L'handle dell'istanza non è valido o fa riferimento a un'istanza di che è stata arrestata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errReadLostFlushVerifyFailure<br />
-1119</p></td>
<td><p>La lettura della pagina del database dal disco presenta una scrittura precedente non rappresentata nella pagina. Disponibile in Windows 8 e versioni successive per il client e Windows Server 2012 e versioni successive per il server.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseDuplicate<br />
-1201</p></td>
<td><p>Il database esiste già.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInUse<br />
-1202</p></td>
<td><p>Database in uso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseNotFound<br />
-1203</p></td>
<td><p>Nessun database di questo tipo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidName<br />
-1204</p></td>
<td><p>Il nome del database non è valido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInvalidPages<br />
-1205</p></td>
<td><p>Numero di pagine non valido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseCorrupted<br />
-1206</p></td>
<td><p>È presente un file non di database o un database danneggiato.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseLocked<br />
-1207</p></td>
<td><p>Il database è bloccato in modo esclusivo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotDisableVersioning<br />
-1208</p></td>
<td><p>Non è possibile disabilitare il controllo delle versioni per questo database.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabaseVersion<br />
-1209</p></td>
<td><p>Il motore di database non è compatibile con il database.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabase200Format<br />
-1210</p></td>
<td><p>Il database è in un formato precedente (200). Questo errore viene restituito da <a href="gg294068(v=exchg.10).md">JetInit</a> se è impostato <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> . Solo client Windows NT.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabase400Format<br />
-1211</p></td>
<td><p>Il database è in un formato precedente (400). Questo errore viene restituito da <a href="gg294068(v=exchg.10).md">JetInit</a> se è impostato <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> . Solo client Windows NT.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabase500Format<br />
-1212</p></td>
<td><p>Il database è in un formato precedente (500). Questo errore viene restituito da <a href="gg294068(v=exchg.10).md">JetInit</a> se è impostato <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> . Solo client Windows NT.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPageSizeMismatch<br />
-1213</p></td>
<td><p>Le dimensioni della pagina del database non corrispondono a quelle del motore.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyInstances<br />
-1214</p></td>
<td><p>Non è possibile avviare altre istanze di database.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseSharingViolation<br />
-1215</p></td>
<td><p>In un'istanza di database diversa viene utilizzato questo database.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errAttachedDatabaseMismatch<br />
-1216</p></td>
<td><p>È stato rilevato un allegato del database in attesa all'inizio o alla fine del ripristino, ma il database è mancante o non corrisponde alle informazioni sugli allegati.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInvalidPath<br />
-1217</p></td>
<td><p>Il percorso specificato per il file di database non è valido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseIdInUse<br />
-1218</p></td>
<td><p>A un database viene assegnato un ID già in uso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errForceDetachNotAllowed<br />
-1219</p></td>
<td><p>Lo scollegamento forzato è consentito solo dopo l'arresto della normale scollegamento a causa di un errore.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCatalogCorrupted<br />
-1220</p></td>
<td><p>È stato rilevato un danneggiamento nel catalogo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPartiallyAttachedDB<br />
-1221</p></td>
<td><p>Il database è collegato solo parzialmente e non è possibile completare l'operazione di connessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseSignInUse<br />
-1222</p></td>
<td><p>Il database con la stessa firma è già in uso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseCorruptedNoRepair<br />
-1224</p></td>
<td><p>Il database è danneggiato ma non è consentito un ripristino.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCreateDbVersion<br />
-1225</p></td>
<td><p>Il motore di database ha tentato di riprodurre un'operazione di creazione database dal log delle transazioni, ma non è riuscito a causa di una versione incompatibile di tale operazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableLocked<br />
-1302</p></td>
<td><p>La tabella è bloccata in modo esclusivo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableDuplicate<br />
-1303</p></td>
<td><p>La tabella esiste già.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableInUse<br />
-1304</p></td>
<td><p>La tabella è in uso e non può essere bloccata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errObjectNotFound<br />
-1305</p></td>
<td><p>Non esiste una tabella o un oggetto di questo tipo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDensityInvalid<br />
-1307</p></td>
<td><p>La densità di un file o un indice non è valida.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableNotEmpty<br />
-1308</p></td>
<td><p>La tabella non è vuota.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidTableId<br />
-1310</p></td>
<td><p>ID di tabella non valido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTables<br />
-1311</p></td>
<td><p>Non è possibile aprire altre tabelle, neanche dopo l'esecuzione dell'attività di pulizia interna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIllegalOperation<br />
-1312</p></td>
<td><p>Operazione non supportata nella tabella.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTablesAndCleanupTimedOut<br />
-1313</p></td>
<td><p>Non è possibile aprire altre tabelle perché il tentativo di pulizia non è stato completato.</p></td>
</tr>
<tr class="even">
<td><p>JET_errObjectDuplicate<br />
-1314</p></td>
<td><p>Il nome della tabella o dell'oggetto è in uso.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidObject<br />
-1316</p></td>
<td><p>L'oggetto non è valido per l'operazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotDeleteTempTable<br />
-1317</p></td>
<td><p>Per eliminare una tabella temporanea, è necessario usare <a href="gg294087(v=exchg.10).md">JetCloseTable</a> anziché <a href="gg294128(v=exchg.10).md">JetDeleteTable</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotDeleteSystemTable<br />
-1318</p></td>
<td><p>Si è verificato un tentativo non valido di eliminare una tabella di sistema.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotDeleteTemplateTable<br />
-1319</p></td>
<td><p>Si è verificato un tentativo non valido di eliminare una tabella del modello.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errExclusiveTableLockRequired<br />
-1322</p></td>
<td><p>Per la tabella deve essere presente un blocco esclusivo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFixedDDL<br />
-1323</p></td>
<td><p>Le operazioni DDL non sono consentite in questa tabella.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFixedInheritedDDL<br />
-1324</p></td>
<td><p>In una tabella derivata, le operazioni DDL non sono consentite sulla parte ereditata del DDL.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotNestDDL<br />
-1325</p></td>
<td><p>La nidificazione della DDL gerarchica non è attualmente supportata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDDLNotInheritable<br />
-1326</p></td>
<td><p>Tentativo di ereditare un DDL da una tabella non contrassegnata come tabella modello.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSettings<br />
-1328</p></td>
<td><p>I parametri di sistema sono stati impostati in modo errato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService<br />
-1329</p></td>
<td><p>Il client ha richiesto l'arresto del servizio.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotAddFixedVarColumnToDerivedTable<br />
-1330</p></td>
<td><p>La tabella modello è stata creata con il flag NoFixedVarColumnsInDerivedTables impostato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexCantBuild<br />
-1401</p></td>
<td><p>Compilazione dell'indice non riuscita.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexHasPrimary<br />
-1402</p></td>
<td><p>L'indice primario è già definito.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexDuplicate<br />
-1403</p></td>
<td><p>L'indice è già definito.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexNotFound<br />
-1404</p></td>
<td><p>Non esiste alcun indice di questo tipo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexMustStay<br />
-1405</p></td>
<td><p>Impossibile eliminare l'indice cluster.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef<br />
-1406</p></td>
<td><p>La definizione dell'indice non è valida.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCreateIndex<br />
-1409</p></td>
<td><p>La creazione della descrizione dell'indice non è valida.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenIndexes<br />
-1410</p></td>
<td><p>Il database non è presente nei blocchi di descrizione dell'indice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMultiValuedIndexViolation<br />
-1411</p></td>
<td><p>Per un indice multivalore sono state generate chiavi di indice inter-record non univoche.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexBuildCorrupted<br />
-1412</p></td>
<td><p>Non è stato possibile compilare un indice secondario che riflette correttamente l'indice primario.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPrimaryIndexCorrupted<br />
-1413</p></td>
<td><p>L'indice primario è danneggiato e il database deve essere deframmentato.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSecondaryIndexCorrupted<br />
-1414</p></td>
<td><p>L'indice secondario è danneggiato e il database deve essere deframmentato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidIndexId<br />
-1416</p></td>
<td><p>ID di indice non valido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesSecondaryIndexOnly<br />
-1430</p></td>
<td><p>L'indice della tupla può essere impostato solo su un indice secondario.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesTooManyColumns<br />
-1431</p></td>
<td><p>La definizione dell'indice per l'indice tupla contiene più colonne chiave che possono essere supportate dal motore di database.</p>
<p><strong>Nota  </strong> Il JET_errIndexTuplesOneColumnOnly errore è obsoleto ed è stato sostituito da JET_errIndexTuplesTooManyColumns.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesNonUniqueOnly<br />
-1432</p></td>
<td><p>L'indice della tupla deve essere un indice non univoco.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesTextBinaryColumnsOnly<br />
-1433</p></td>
<td><p>Una definizione di indice tupla può contenere solo colonne chiave con tipi di colonna di testo o binari.</p>
<p><strong>Nota  </strong> Il JET_errIndexTuplesTextColumnsOnly errore è obsoleto ed è stato sostituito da JET_errIndexTuplesTextBinaryColumnsOnly.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesVarSegMacNotAllowed<br />
-1434</p></td>
<td><p>L'indice della tupla non consente l'impostazione di cbVarSegMac.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesInvalidLimits<br />
-1435</p></td>
<td><p>La lunghezza minima o massima della tupla o il numero massimo di caratteri specificati per un indice non sono validi.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesCannotRetrieveFromIndex<br />
-1436</p></td>
<td><p>Impossibile chiamare <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> con il flag di JET_bitRetrieveFromIndex impostato durante il recupero di una colonna in un indice di tupla.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesKeyTooSmall<br />
-1437</p></td>
<td><p>La chiave specificata non soddisfa la lunghezza minima della tupla.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnLong<br />
-1501</p></td>
<td><p>Il valore della colonna è Long.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNoChunk<br />
-1502</p></td>
<td><p>Non esiste un blocco di questo tipo in un valore Long.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnDoesNotFit<br />
-1503</p></td>
<td><p>Il campo non rientrerà nel record.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNullInvalid<br />
-1504</p></td>
<td><p>Null non valido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnIllegalNull<br />
JET_errNullInvalid</p></td>
<td><p>Null non valido. Questo errore viene restituito da Gestione record.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnIndexed-1505</p></td>
<td><p>La colonna è indicizzata e non può essere eliminata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnTooBig-1506</p></td>
<td><p>La lunghezza del campo è maggiore della lunghezza massima consentita.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound-1507</p></td>
<td><p>Non esiste alcuna colonna di questo tipo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnDuplicate-1508</p></td>
<td><p>Questo campo è già definito.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMultiValuedColumnMustBeTagged-1509</p></td>
<td><p>È stato effettuato un tentativo di creare una colonna multivalore, ma la colonna non è stata contrassegnata con tag.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnRedundant-1510</p></td>
<td><p>È presente una seconda colonna con incremento automatico o versione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType-1511</p></td>
<td><p>Il tipo di dati della colonna non è valido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTaggedNotNULL-1514</p></td>
<td><p>Non sono presenti colonne con tag non NULL.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentIndex-1515</p></td>
<td><p>Il database non è valido perché non contiene un indice corrente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyIsMade-1516</p></td>
<td><p>La chiave è stata completata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadColumnId-1517</p></td>
<td><p>ID di colonna non corretto.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadItagSequence-1518</p></td>
<td><p>ItagSequence non valido per la colonna con tag.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnInRelationship-1519</p></td>
<td><p>Una colonna non può essere eliminata perché fa parte di una relazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotBeTagged-1521</p></td>
<td><p>Impossibile contrassegnare l'incremento automatico e la versione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDefaultValueTooBig-1524</p></td>
<td><p>Il valore predefinito supera la dimensione massima.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMultiValuedDuplicate-1525</p></td>
<td><p>È stato rilevato un valore duplicato in una colonna multivalore univoca.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLVCorrupted-1526</p></td>
<td><p>È stato rilevato un danneggiamento in un albero con valori Long.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMultiValuedDuplicateAfterTruncation-1528</p></td>
<td><p>È stato rilevato un valore duplicato in una colonna univoca multivalore dopo che i dati sono stati normalizzati e la normalizzazione dei dati è stata troncata prima del confronto.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDerivedColumnCorruption-1529</p></td>
<td><p>Colonna non valida nella tabella derivata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPlaceholderColumn-1530</p></td>
<td><p>È stato effettuato un tentativo di convertire una colonna in un segnaposto di indice primario, ma la colonna non soddisfa i criteri necessari.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordNotFound-1601</p></td>
<td><p>Chiave non trovata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordNoCopy-1602</p></td>
<td><p>Nessun buffer funzionante.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord-1603</p></td>
<td><p>Non è presente nessun record corrente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordPrimaryChanged-1604</p></td>
<td><p>È possibile che la chiave primaria non venga modificata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyDuplicate-1605</p></td>
<td><p>Chiave duplicata non valida.</p></td>
</tr>
<tr class="even">
<td><p>JET_errAlreadyPrepared-1607</p></td>
<td><p>È stato effettuato un tentativo di aggiornare un record mentre era già in corso un aggiornamento del record.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyNotMade-1608</p></td>
<td><p>Non è stata effettuata alcuna chiamata a <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errUpdateNotPrepared-1609</p></td>
<td><p>Non è stata effettuata alcuna chiamata a <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDataHasChanged-1611</p></td>
<td><p>I dati sono stati modificati e l'operazione è stata interrotta.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLanguageNotSupported-1619</p></td>
<td><p>Questa installazione di Windows non supporta la lingua selezionata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManySorts-1701</p></td>
<td><p>Troppi processi di ordinamento.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidOnSort-1702</p></td>
<td><p>Si è verificata un'operazione non valida durante un ordinamento.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTempFileOpenError-1803</p></td>
<td><p>Non è stato possibile aprire il file temporaneo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyAttachedDatabases-1805</p></td>
<td><p>Troppi database aperti.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDiskFull-1808</p></td>
<td><p>Spazio su disco insufficiente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPermissionDenied-1809</p></td>
<td><p>Autorizzazione negata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound-1811</p></td>
<td><p>Impossibile trovare il file.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileInvalidType-1812</p></td>
<td><p>Il tipo di file non è valido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errAfterInitialization-1850</p></td>
<td><p>Non è possibile avviare un ripristino dopo l'inizializzazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogCorrupted-1852</p></td>
<td><p>Non è stato possibile interpretare i log.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidOperation-1906</p></td>
<td><p>Operazione non valida.</p></td>
</tr>
<tr class="even">
<td><p>JET_errAccessDenied-1907</p></td>
<td><p>Accesso negato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManySplits-1909</p></td>
<td><p>Divisione infinita.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation-1910</p></td>
<td><p>Più thread utilizzano la stessa sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errEntryPointNotFound-1911</p></td>
<td><p>Impossibile trovare un punto di ingresso in una DLL obbligatoria.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionContextAlreadySet-1912</p></td>
<td><p>Per la sessione specificata è già impostato un contesto di sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionContextNotSetByThisThread-1913</p></td>
<td><p>È stato eseguito un tentativo di reimpostare il contesto della sessione, ma il thread corrente non è quello originale che ha impostato il contesto della sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionInUse-1914</p></td>
<td><p>È stato effettuato un tentativo di terminare la sessione attualmente in uso.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordFormatConversionFailed-1915</p></td>
<td><p>Si è verificato un errore interno durante una conversione del formato di record dinamico.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOneDatabasePerSession-1916</p></td>
<td><p>È consentito un solo database utente aperto per sessione, come indicato impostando il flag di <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> durante la creazione del database.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRollbackError-1917</p></td>
<td><p>Si è verificato un errore durante il rollback.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCallbackFailed-2101</p></td>
<td><p>Chiamata di funzione di callback non riuscita.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCallbackNotResolved-2102</p></td>
<td><p>Una funzione di callback non è stata trovata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotInvalidSequence-2401</p></td>
<td><p>L'API copia shadow del sistema operativo è stata usata in una sequenza non valida.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotTimeOut-2402</p></td>
<td><p>La copia shadow del sistema operativo è terminata con un timeout.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotNotAllowed-2403</p></td>
<td><p>La copia shadow del sistema operativo non è consentita perché è stato eseguito un backup o un ripristino in.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSnapId-2404</p></td>
<td><p>L'operazione non è riuscita perché l'handle di copia shadow del sistema operativo specificato non è valido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLSCallbackNotSpecified-3000</p></td>
<td><p>È stato effettuato un tentativo di usare l'archiviazione locale senza una funzione di callback specificata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLSAlreadySet-3001</p></td>
<td><p>È stato effettuato un tentativo di impostare l'archiviazione locale per un oggetto per cui è già stato impostato.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLSNotSet-3002</p></td>
<td><p>È stato effettuato un tentativo di recuperare l'archiviazione locale da un oggetto che non è stato impostato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileIOSparse-4000</p></td>
<td><p>Un'operazione di I/O non è riuscita perché è stata tentata in un'area non allocata di un file.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileIOBeyondEOF-4001</p></td>
<td><p>Una lettura è stata rilasciata in una posizione successiva alla EOF (le Scritture espanderanno il file).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileIOAbort-4002</p></td>
<td><p>Questo flag indica al chiamante del JET_ABORTRETRYFAILCALLBACK di interrompere l'i/O specificato.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileIORetry-4003</p></td>
<td><p>Questo flag indica al chiamante del JET_ABORTRETRYFAILCALLBACK di ritentare l'i/O specificato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileIOFail-4004</p></td>
<td><p>Questo flag indica al chiamante del JET_ABORTRETRYFAILCALLBACK di non eseguire l'i/O specificato.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileCompressed-4005</p></td>
<td><p>L'accesso in lettura/scrittura non è supportato nei file compressi.</p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a>Commenti

In generale, un valore maggiore di zero deve essere interpretato come un avviso, un valore pari a zero deve essere interpretato come esito positivo e un valore minore di zero deve essere interpretato come un errore. Nessun altro modello in questi valori, ad esempio intervalli di valori, deve essere basato su un'applicazione.

### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[Parametri di gestione degli errori](./error-handling-parameters.md)  
[Errori del motore di archiviazione estendibile](./extensible-storage-engine-errors.md)  
[File del motore di archiviazione estendibile](./extensible-storage-engine-files.md)
