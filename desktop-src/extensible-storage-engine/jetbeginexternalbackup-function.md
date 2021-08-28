---
description: 'Altre informazioni su: Funzione JetBeginExternalBackup'
title: Funzione JetBeginExternalBackup
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
ms.openlocfilehash: 8d0e47a117c044899a8b078290be622cfecdae91
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482907"
---
# <a name="jetbeginexternalbackup-function"></a>Funzione JetBeginExternalBackup


_**Si applica a:** Windows | Windows Server_

## <a name="jetbeginexternalbackup-function"></a>Funzione JetBeginExternalBackup

La **funzione JetBeginExternalBackup** avvia un backup esterno mentre il motore e il database sono online e attivi. **JetBeginExternalBackup** è il primo di una serie di funzioni che devono essere chiamate per eseguire correttamente un backup online (non basato su VSS).

Un backup esterno può essere usato per implementare backup completi, incrementali o differenziali.

Il backup sarà fuzzy, in quanto il backup sarà coerente con un singolo punto nel tempo nella cronologia delle transazioni, ma non è possibile controllare il punto esatto nel tempo.

```cpp
    JET_ERR JET_API JetBeginExternalBackup(
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*grbit*

Gruppo di bit che specificano zero o più delle opzioni seguenti.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitBackupAtomic</p> | <p>Questo flag è deprecato. L'utilizzo di questo bit comporta la JET_errInvalidgrbit restituita.</p> | 
| <p>JET_bitBackupIncremental</p> | <p>Crea un backup incrementale anziché un backup completo. Ciò significa che verrà eseguito il backup solo dei file di log dall'ultimo backup completo o incrementale.</p> | 
| <p>JET_bitBackupSnapshot</p> | <p>Riservato per utilizzi futuri. Definito per Windows XP.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBackupInProgress</p> | <p>Se è già in corso un backup esterno o un backup di snapshot, verrà restituito questo errore finché non viene chiamato <strong>JetBeginExternalBackup</strong> (o una delle relative varianti). ESE consente un solo backup online alla volta.</p> | 
| <p>JET_errBackupNotAllowedYet</p> | <p>L'istanza o il motore di database è in fase di recupero o di arresto o chiusura.</p> | 
| <p>JET_errCheckpointCorrupt</p> | <p>In un backup completo non è stato possibile leggere il file del checkpoint o verificare il file.</p> | 
| <p>JET_errCheckpointFileNotFound</p> | <p>In un backup completo non è stato possibile trovare il file del checkpoint.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>L'operazione non può essere completata perché tutte le attività nell'istanza associata alla sessione sono scadute in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>L'operazione non può essere completata perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p><strong>Windows XP:</strong> Questo valore restituito è stato introdotto in Windows XP.</p> | 
| <p>JET_errInvalidBackup</p> | <p>La registrazione circolare è abilitata e il tipo di backup specificato è JET_bitBackupIncremental. Per <a href="gg269235(v=exchg.10).md">informazioni su come controllare la</a> registrazione circolare o non <strong>circolare,</strong> vedere JET_paramCircularLog in Errori del log delle transazioni.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Uno o più membri <em>grbit</em> non sono validi.</p> | 
| <p>JET_errLoggingDisabled</p> | <p>Il ripristino o la registrazione è disabilitata. Non è possibile eseguire un backup online se la registrazione è disabilitata. Per altre informazioni sulla registrazione e il ripristino, <a href="gg269235(v=exchg.10).md">vedere JET_paramRecovery</a>.</p> | 
| <p>JET_errLogWriteFail</p> | <p>Il motore ha interrotto la scrittura nell'unità di log a causa di errori di I/O del disco o del log pieno.</p> | 
| <p>JET_errMissingFullBackup</p> | <p>Il backup incrementale è stato specificato (con JET_bitBackupIncremental) e non è mai stato eseguito un backup completo per uno dei database collegati per il set di registrazione.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errOutOfMemory</p> | <p>L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per completarla.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Impossibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità Windows 2000) in cui è supportata una sola istanza quando in realtà esistono già più istanze.</p> | 
| <p>JET_errTermInProgress</p> | <p>Impossibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



Se la funzione ha esito positivo, viene avviato un backup esterno e viene inizializzato il motore di stato del backup. È ora possibile chiamare le API successive per completare la sequenza di backup esterna e trasmettere o leggere il file di database, il file di patch del database (se supportato) e il file di log. È possibile che sia stato registrato un evento che indica l'inizio di un backup esterno.

Se la funzione ha esito negativo, la sessione di backup non verrà avviata. Se è in corso un'altra sessione di backup, non verrà annullata.

#### <a name="remarks"></a>Commenti

Il processo di backup esterno (avviato da **JetBeginExternalBackup)** è progettato per consentire un backup online delle transazioni fuzzy dell'intera istanza in un dispositivo di destinazione come flusso. Il backup conterrà tutti i file di database collegati all'istanza tramite [JetAttachDatabase](./jetattachdatabase-function.md) (per un backup completo), seguiti dai file di patch del database associati (se supportati) e infine dai file di log delle transazioni generati durante il processo di backup. Il risultato finale sarà un set di file che possono essere ripristinati dal flusso, eventualmente combinati con i file di database e di log esistenti, e infine ripristinati in uno stato coerente.

L'ordine generale delle operazioni per un backup completo è costituito dalle chiamate seguenti. In primo **luogo, viene chiamato JetBeginExternalBackup** per avviare il processo di backup. Viene quindi [chiamato JetGetAttachInfo](./jetgetattachinfo-function.md) per ottenere l'elenco dei database collegati all'istanza di di cui è necessario eseguire il backup. Per ognuno di questi database, viene chiamato [JetOpenFile,](./jetopenfile-function.md) seguito da una serie di chiamate [JetReadFile](./jetreadfile-function.md) e quindi da una chiamata a [JetCloseFile.](./jetclosefile-function.md) Viene quindi [chiamato JetGetLogInfo](./jetgetloginfo-function.md) per ottenere un elenco di file di log e patch di database di cui eseguire il backup. Per ognuno di questi file, viene effettuata un'altra sequenza di chiamate [JetOpenFile,](./jetopenfile-function.md) [JetReadFile](./jetreadfile-function.md)e [JetCloseFile.](./jetclosefile-function.md) Quindi, tutti i file di log delle transazioni indesiderati vengono eliminati [usando JetTruncateLog](./jettruncatelog-function.md). Infine, il backup viene terminato da una chiamata a [JetEndExternalBackup.](./jetendexternalbackup-function.md)

È anche possibile modificare questo set di passaggi per eseguire un backup incrementale dell'istanza. Un backup incrementale enumera ed esegue il backup dei file di log. I backup incrementali sono possibili solo se la registrazione circolare non è abilitata.

È anche possibile modificare questo set di passaggi per consentire l'esecuzione di backup differenziali successivi dell'istanza. Per eseguire un backup differenziale, non chiamare [JetTruncateLog](./jettruncatelog-function.md) nel backup completo o incrementale precedente. Se non si chiama [JetTruncateLog](./jettruncatelog-function.md), si abilitano i backup successivi come differenziali rispetto all'ultimo backup completo o incrementale. I backup differenziali sono possibili solo se la registrazione circolare non è abilitata.

Il file di patch del database è un file ausiliario speciale usato per archiviare le immagini delle pagine del database in determinate circostanze durante il backup. Questo file deve essere presente nello stesso percorso del database associato durante un'operazione di ripristino. Questo file viene usato solo in Windows 2000. Di conseguenza, qualsiasi applicazione scritta per funzionare con Windows 2000 e altre versioni deve supportare i file di patch del database, se presenti, ma non deve avere esito negativo se non sono presenti.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



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
