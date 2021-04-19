---
description: 'Altre informazioni su: funzione JetBeginExternalBackup'
title: JetBeginExternalBackup (funzione)
TOCTitle: JetBeginExternalBackup Function
ms:assetid: 702e6cbf-4648-40f2-b2eb-6194759d4cde
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269292(v=EXCHG.10)
ms:contentKeyID: 32765584
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d410adb592c3d56d2f9880ec809749396318258a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318100"
---
# <a name="jetbeginexternalbackup-function"></a>JetBeginExternalBackup (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetbeginexternalbackup-function"></a>JetBeginExternalBackup (funzione)

La funzione **JetBeginExternalBackup** avvia un backup esterno mentre il motore e il database sono online e attivi. **JetBeginExternalBackup** è il primo di una serie di funzioni che devono essere chiamate per eseguire un backup online (non basato su VSS) riuscito.

Un backup esterno può essere utilizzato per implementare backup completi, incrementali o differenziali.

Il backup sarà fuzzy, in quanto il backup sarà coerente a un singolo momento della cronologia delle transazioni, ma non è possibile controllare il punto nel tempo esatto.

```cpp
    JET_ERR JET_API JetBeginExternalBackup(
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*grbit*

Gruppo di bit che specifica zero o più delle opzioni seguenti.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valore</p></th>
<th><p>Significato</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitBackupAtomic</p></td>
<td><p>Questo flag è deprecato. L'utilizzo di questo bit comporterà la restituzione JET_errInvalidgrbit.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitBackupIncremental</p></td>
<td><p>Crea un backup incrementale anziché un backup completo. Ciò significa che verrà eseguito il backup solo dei file di log dall'ultimo backup completo o incrementale.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitBackupSnapshot</p></td>
<td><p>Riservato per utilizzi futuri. Definito per Windows XP.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti. Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Codice restituito</p></th>
<th><p>Descrizione</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Operazione riuscita.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupInProgress</p></td>
<td><p>Se è già in corso un backup o un backup di snapshot esterno, verrà restituito questo errore fino a quando non viene chiamato <strong>JetBeginExternalBackup</strong> (o una delle varianti). ESE consente un solo backup online alla volta.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBackupNotAllowedYet</p></td>
<td><p>L'istanza o il motore di database è in fase di ripristino oppure in fase di arresto o chiusura.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCheckpointCorrupt</p></td>
<td><p>In un backup completo non è stato possibile leggere il file del checkpoint oppure il file non è stato verificato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCheckpointFileNotFound</p></td>
<td><p>In un backup completo non è stato possibile trovare il file del checkpoint.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</p>
<p><strong>Windows XP:  </strong> Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBackup</p></td>
<td><p>La registrazione circolare è abilitata e il tipo di backup specificato viene JET_bitBackupIncremental. Per informazioni su come controllare la registrazione circolare o non circolare, vedere <a href="gg269235(v=exchg.10).md">JET_paramCircularLog</a> negli <strong>errori del log delle transazioni</strong> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Uno o più membri di <em>grbit</em> non sono validi.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLoggingDisabled</p></td>
<td><p>Il ripristino o la registrazione è disabilitata. Se la registrazione è disabilitata, non è possibile eseguire un backup in linea. Per ulteriori informazioni sulla registrazione e il ripristino, vedere <a href="gg269235(v=exchg.10).md">JET_paramRecovery</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogWriteFail</p></td>
<td><p>Il motore ha smesso di scrivere nell'unità di log, a causa di errori di i/o del disco e completi.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingFullBackup</p></td>
<td><p>Il backup incrementale è stato specificato (con JET_bitBackupIncremental) e non è mai stato eseguito un backup completo per uno dei database collegati per il set di registrazione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per il completamento.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza quando sono già presenti più istanze.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p></td>
</tr>
</tbody>
</table>


Se la funzione ha esito positivo, viene avviato un backup esterno e viene inizializzato il motore dello stato di backup. È ora possibile chiamare le API successive per completare la sequenza di backup esterna e trasmettere o leggere il file di database, il file di patch del database (se supportato) e il file di log. È possibile registrare un evento in cui è stato avviato un backup esterno.

Se la funzione ha esito negativo, la sessione di backup non verrà avviata. Se è in corso un'altra sessione di backup, non verrà annullata.

#### <a name="remarks"></a>Commenti

Il processo di backup esterno, come avviato da **JetBeginExternalBackup**, è progettato per consentire a un dispositivo di destinazione un backup di transazione fuzzy dell'intera istanza in un dispositivo di destinazione come flusso. Il backup conterrà tutti i file di database collegati all'istanza di utilizzando [JetAttachDatabase](./jetattachdatabase-function.md) (per un backup completo), seguiti dai file di patch del database associati (se supportati) e infine dai file di log delle transazioni generati durante il processo di backup. Il risultato finale sarà un set di file che possono essere ripristinati dal flusso, possibilmente combinati con i file di database e di log esistenti e infine ripristinati in uno stato coerente.

L'ordine generale delle operazioni per un backup completo è costituito dalle chiamate seguenti. In primo luogo, **JetBeginExternalBackup** viene chiamato per avviare il processo di backup. Viene quindi chiamato [JetGetAttachInfo](./jetgetattachinfo-function.md) per ottenere l'elenco di database collegati all'istanza di di cui è necessario eseguire il backup. Per ognuno di questi database, viene chiamato [JetOpenFile](./jetopenfile-function.md) , seguito da una serie di chiamate [JetReadFile](./jetreadfile-function.md) e quindi da una chiamata a [JetCloseFile](./jetclosefile-function.md). Viene quindi chiamato [JetGetLogInfo](./jetgetloginfo-function.md) per ottenere un elenco dei file di patch e di log del database di cui eseguire il backup. Per ognuno di questi file viene effettuata un'altra sequenza di chiamate a [JetOpenFile](./jetopenfile-function.md), [JetReadFile](./jetreadfile-function.md)e [JetCloseFile](./jetclosefile-function.md) . Quindi, eventuali file di log delle transazioni indesiderati vengono eliminati utilizzando [JetTruncateLog](./jettruncatelog-function.md). Infine, il backup viene terminato con una chiamata a [JetEndExternalBackup](./jetendexternalbackup-function.md).

È anche possibile modificare questa serie di passaggi per eseguire un backup incrementale dell'istanza. Un backup incrementale enumera ed esegue il backup dei file di log. I backup incrementali sono possibili solo se la registrazione circolare non è abilitata.

È anche possibile modificare questa serie di passaggi per consentire l'esecuzione di backup differenziali successivi dell'istanza. Per eseguire un backup differenziale, non chiamare [JetTruncateLog](./jettruncatelog-function.md) nel backup completo o incrementale precedente. Se non si chiama [JetTruncateLog](./jettruncatelog-function.md), i backup successivi vengono abilitati come differenziali rispetto all'ultimo backup completo o incrementale. I backup differenziali sono possibili solo se la registrazione circolare non è abilitata.

Il file di patch del database è un file ausiliario speciale usato per archiviare le immagini della pagina del database in determinate circostanze durante il backup. Questo file deve essere presente nella stessa posizione del database associato durante un'operazione di ripristino. Questo file viene usato solo in Windows 2000. Di conseguenza, tutte le applicazioni scritte per funzionare con Windows 2000 e altre versioni devono supportare i file delle patch del database, se sono presenti, ma anche non devono avere esito negativo se non sono presenti.

#### <a name="requirements"></a>Requisiti

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
<tr class="even">
<td><p><strong>Libreria</strong></p></td>
<td><p>Usare ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Richiede ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JetEndExternalBackup](./jetendexternalbackup-function.md)  
[JetEndExternalBackupInstance2](./jetendexternalbackupinstance2-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)
