---
description: Altre informazioni sulla funzione JetExternalRestore2
title: Funzione JetExternalRestore2
TOCTitle: JetExternalRestore2 Function
ms:assetid: 66331be0-7abc-43a0-8b8b-dbdd227c918e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269272(v=EXCHG.10)
ms:contentKeyID: 32765574
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetExternalRestore2W
- JetExternalRestore2A
- JetExternalRestore2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: adceb414fdea434f84178a6e4f0b8b33838e954d
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987434"
---
# <a name="jetexternalrestore2-function"></a>Funzione JetExternalRestore2


_**Si applica a:** Windows | Windows Server_

## <a name="jetexternalrestore2-function"></a>Funzione JetExternalRestore2

La **funzione JetExternalRestore2** ripristina un backup esterno eseguito con le API di backup esterne e fornisce checkpoint da usare per le operazioni di registrazione circolare. Questa operazione è nota come ripristino a tempo indeterminato, che è simile ma diverso dal recupero a tempo indeterminato eseguito [dalla funzione JetInit.](./jetinit-function.md)

**Windows XP: JetExternalRestore2** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetExternalRestore2(
      __in          JET_PSTR szCheckpointFilePath,
      __in          JET_PSTR szLogPath,
      __in_opt      JET_RSTMAP* rgrstmap,
      __in          long crstfilemap,
      __in          JET_PSTR szBackupLogPath,
      __in_out      JET_LOGINFO* pLogInfo,
      __in_opt      JET_PSTR szTargetInstanceName,
      __in_opt      JET_PSTR szTargetInstanceLogPath,
      __in_opt      JET_PSTR szTargetInstanceCheckpointPath,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a>Parametri

*szCheckpointFilePath*

Percorso del file del checkpoint da usare durante il ripristino se *szTargetInstanceCheckpointPath* non è specificato o il percorso ha un'istanza attiva o in esecuzione.

*szLogPath*

Percorso o directory dei log per la fase finale (annullamento) del ripristino ed eventualmente per i log di roll forward. Questo percorso può essere lo stesso di *szBackupLogPath*.

*rgrstmap*

Si tratta di una matrice [JET_RSTMAP](./jet-rstmap-structure.md) strutture . Si tratta di una mappa di percorsi o nomi file di database nuovi e vecchi. Viene usato perché potrebbe essere necessario ripristinare i database in un percorso diverso da quello da cui è stato eseguito il backup. Nel caso in cui più database siano collegati a un singolo set di registrazione, la mappa di ripristino può specificare un subset dei database da ripristinare.

*crstfilemap*

Numero di voci nel parametro *di matrice rgrstmap.*

*szBackupLogPath*

Percorso della directory in cui vengono ripristinati i file di log. Si tratta dei log letti durante la sequenza di backup esterna. Questo percorso può essere lo stesso di *szLogPath.*

*pLogInfo*

*PLogInfo* descrive diversi aspetti dei log di backup per il ripristino. Questo parametro consente a **JetExternalRestore2** di usare i parametri *genLow* e *genHigh* espliciti di **JetExternalRestore2,** nonché il nome del log di base, anziché il nome di base del log "edb".

*szTargetInstanceName*

Questo parametro è deprecato e non può essere usato nell'applicazione.

*szTargetInstanceLogPath*

Percorso dei log di roll forward se il percorso dei log di cui si vuole eseguire il roll forward si verifica in un set di registrazione attivo o in un'istanza di . Non deve essere specificato se l'istanza di destinazione usa la registrazione circolare.

*szTargetInstanceCheckpointPath*

Percorso del checkpoint durante il ripristino se non è presente alcuna istanza attiva in esecuzione in questa destinazione. Non deve essere specificato se l'istanza di destinazione usa la registrazione circolare.

*Pfn*

Callback di stato, che segnala lo stato di avanzamento del ripristino.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBadRestoreTargetInstance</p> | <p>Il <em>valore szTargetInstanceLogPath</em> specificato non appartiene a un'istanza inizializzata. Questo errore verrà restituito solo in Windows XP e versioni successive.</p> | 
| <p>JET_errDatabaseCorrupted</p> | <p>Ciò indica che il database è danneggiato o un file non riconosciuto.</p> | 
| <p>JET_errEndingRestoreLogTooLow</p> | <p>Questo errore viene restituito se uno dei file di log in <em>szBackupLogPath</em>ha una generazione di log superiore a quella specificata in <em>genHigh</em> o <em>pLogInfo.ulGenHigh.</em></p> | 
| <p>JET_errFileNotFound</p> | <p>L'operazione non è riuscita perché non è stato possibile aprire il file richiesto perché non è stato trovato nel percorso specificato.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro. Questa operazione può verificarsi per <a href="gg294088(v=exchg.10).md">JetExternalRestore</a>e così via quando <em>szTargetCheckpointPath</em> e <em>szTargetInstanceLogPath</em> non sono entrambi specificati o non sono entrambi non specificati. In altri casi, devono corrispondere ed essere entrambi specificati o entrambi non specificati.</p> | 
| <p>JET_errInvalidPath</p> | <p>L'operazione non è riuscita perché non è stato possibile trovare il percorso specificato.</p> | 
| <p>JET_errOutOfMemory</p> | <p>L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per completarla.</p> | 
| <p>JET_errRestoreOfNonBackupDatabase</p> | <p>Questo errore viene restituito se il file di database specificato durante il ripristino non è un database di cui è stato eseguito il backup esterno.</p> | 
| <p>JET_errRunningInOneInstanceMode</p> | <p>Il motore di database non può eseguire il ripristino esterno o il ripristino a disco rigido in modalità istanza singola. Questo errore verrà restituito solo in Windows XP e versioni successive.</p> | 
| <p>JET_errStartingRestoreLogTooHigh</p> | <p>Questo errore viene restituito se uno dei file di log in <em>szBackupLogPath</em>ha una generazione di log inferiore a quella specificata da <em>genLow</em> o <em>pLogInfo.ulGenLow.</em></p> | 



In caso di esito positivo, tutti i database di *rgrstmap* vengono ripristinati completamente e in uno stato pulito o coerente. A questo punto il database può essere rimontato in un'istanza esistente.

In caso di errore, il motore non è riuscito a recuperare il database. Il database è in uno stato non valido e per ritentare il ripristino a prova l'intero database deve essere ripristinato nuovamente. In genere, l'origine di una situazione di questo tipo è il danneggiamento del disco o del log o un'altra forma di gestione errata del log o un set di log non continuo.

#### <a name="remarks"></a>Commenti

Vedere [JetExternalRestore.](./jetexternalrestore-function.md)

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetExternalRestore2W</strong> (Unicode) e <strong>JetExternalRestore2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetExternalRestore](./jetexternalrestore-function.md)  
[JetInit](./jetinit-function.md)
