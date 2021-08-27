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
ms.openlocfilehash: ad8cad0cfc31c77b3cc8e960153bda14b4f431e5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475817"
---
# <a name="jetexternalrestore2-function"></a>Funzione JetExternalRestore2


_**Si applica a:** Windows | Windows Server_

## <a name="jetexternalrestore2-function"></a>Funzione JetExternalRestore2

La **funzione JetExternalRestore2** ripristina un backup esterno eseguito con le API di backup esterne e fornisce checkpoint da usare per le operazioni di registrazione circolare. Questa operazione è nota come ripristino rigido, che è simile ma diverso dal ripristino soft eseguito dalla [funzione JetInit.](./jetinit-function.md)

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

Percorso o directory per i log per la fase finale (annullamento) del ripristino ed eventualmente per i log di roll forward. Questo percorso può essere lo stesso di *szBackupLogPath*.

*rgrstmap*

Si tratta di una matrice [di JET_RSTMAP](./jet-rstmap-structure.md) struttura. Si tratta di una mappa di percorsi o nomi di file di database vecchi e nuovi. Viene usato perché potrebbe essere necessario ripristinare i database in un percorso diverso da quello da cui è stato eseguito il backup. Nel caso in cui più database siano collegati a un singolo set di registrazione, la mappa di ripristino può specificare un subset dei database da ripristinare.

*crstfilemap*

Numero di voci nel parametro della matrice *rgrstmap.*

*szBackupLogPath*

Percorso della directory in cui vengono ripristinati i file di log. Si tratta dei log letti durante la sequenza di backup esterna. Questo percorso può essere lo stesso di *szLogPath*.

*pLogInfo*

*PLogInfo* descrive diversi aspetti dei log di backup da recuperare. Questo parametro consente a **JetExternalRestore2** di usare i parametri *genLow* e *genHigh* espliciti di **JetExternalRestore2,** nonché il nome del log di base, anziché un nome di base del log presunto di "edb".

*szTargetInstanceName*

Questo parametro è deprecato e non può essere usato nell'applicazione.

*szTargetInstanceLogPath*

Percorso per i log di roll forward se il percorso dei log da eseguire è in un'istanza o in un set di registrazione attivo. Questa opzione non deve essere specificata se l'istanza di destinazione usa la registrazione circolare.

*szTargetInstanceCheckpointPath*

Percorso del checkpoint durante il ripristino se non è presente alcuna istanza attiva in esecuzione in questa destinazione. Questa opzione non deve essere specificata se l'istanza di destinazione usa la registrazione circolare.

*Pfn*

Callback di stato, che segnala lo stato di avanzamento del ripristino.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBadRestoreTargetInstance</p> | <p><em>SzTargetInstanceLogPath specificato</em> non appartiene a un'istanza inizializzata. Questo errore verrà restituito solo in Windows XP e versioni successive.</p> | 
| <p>JET_errDatabaseCorrupted</p> | <p>Ciò indica che il database è stato danneggiato o un file non riconosciuto.</p> | 
| <p>JET_errEndingRestoreLogTooLow</p> | <p>Questo errore viene restituito se per uno dei file di log in <em>szBackupLogPath</em>è presente una generazione di log superiore a quella specificata in <em>genHigh</em> o <em>pLogInfo.ulGenHigh</em>.</p> | 
| <p>JET_errFileNotFound</p> | <p>L'operazione non è riuscita perché non è stato possibile aprire il file richiesto perché non è stato trovato nel percorso specificato.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti conteneva un valore imprevisto o conteneva un valore che non aveva senso se combinato con il valore di un altro parametro. Ciò può verificarsi per <a href="gg294088(v=exchg.10).md">JetExternalRestore</a>e così via quando <em>szTargetCheckpointPath</em> e <em>szTargetInstanceLogPath</em> non sono entrambi specificati o non entrambi non specificati. In altri casi, devono corrispondere ed essere entrambi specificati o entrambi non specificati.</p> | 
| <p>JET_errInvalidPath</p> | <p>L'operazione non è riuscita perché non è stato possibile trovare il percorso specificato.</p> | 
| <p>JET_errOutOfMemory</p> | <p>L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per completarla.</p> | 
| <p>JET_errRestoreOfNonBackupDatabase</p> | <p>Questo errore viene restituito se il file di database specificato durante il ripristino non è un database di cui è stato eseguito il backup esterno.</p> | 
| <p>JET_errRunningInOneInstanceMode</p> | <p>Il motore di database non può eseguire il ripristino esterno o il ripristino rigido in modalità a istanza singola. Questo errore verrà restituito solo in Windows XP e versioni successive.</p> | 
| <p>JET_errStartingRestoreLogTooHigh</p> | <p>Questo errore viene restituito se uno dei file di log in <em>szBackupLogPath</em>ha una generazione di log inferiore a quella specificata da <em>genLow</em> o <em>pLogInfo.ulGenLow</em>.</p> | 



In caso di esito positivo, tutti i database di *rgrstmap* vengono completamente ripristinati e in uno stato pulito o coerente. A questo punto il database può essere rimontaggio in un'istanza esistente.

In caso di errore, il motore non è riuscito a ripristinare il database. Il database è in uno stato non valido e per ritentare il ripristino rigido è necessario ripristinare nuovamente l'intero database. In genere, l'origine di una situazione di questo tipo è il danneggiamento del disco o del log o un'altra forma di gestione errata del log o di un set di log non continuo.

#### <a name="remarks"></a>Commenti

Vedere [JetExternalRestore](./jetexternalrestore-function.md).

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetExternalRestore2W</strong> (Unicode) e <strong>JetExternalRestore2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetExternalRestore](./jetexternalrestore-function.md)  
[JetInit](./jetinit-function.md)
