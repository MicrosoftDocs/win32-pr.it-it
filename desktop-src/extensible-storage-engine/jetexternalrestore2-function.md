---
description: 'Altre informazioni su: funzione JetExternalRestore2'
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
ms.openlocfilehash: c96314e401a81271f5a71bc056faa95fc1ae0dbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967949"
---
# <a name="jetexternalrestore2-function"></a>Funzione JetExternalRestore2


_**Si applica a:** Windows | Windows Server_

## <a name="jetexternalrestore2-function"></a>Funzione JetExternalRestore2

La funzione **JetExternalRestore2** ripristina un backup esterno che è stato usato con le API di backup esterne e fornisce checkpoint da usare per le operazioni di registrazione circolari. Questa operazione è nota come ripristino a livello di hardware, che è simile ma differente rispetto al ripristino soft eseguito dalla funzione [JetInit](./jetinit-function.md) .

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

Percorso del file del checkpoint da utilizzare durante il ripristino se *szTargetInstanceCheckpointPath* non è specificato o se il percorso dispone di un'istanza attiva o in esecuzione.

*szLogPath*

Percorso o directory dei log per la fase finale (annullamento) del ripristino ed eventualmente per i log di rollforward. Questo percorso può essere uguale a quello di *szBackupLogPath*.

*rgrstmap*

Si tratta di una matrice di strutture di [JET_RSTMAP](./jet-rstmap-structure.md) . Si tratta di una mappa di percorsi di database vecchi e nuovi o di nomi file. Questa operazione viene utilizzata perché potrebbe essere necessario ripristinare i database in un percorso diverso da quello di cui è stato eseguito il backup. Nel caso in cui più database siano collegati a un singolo set di registrazione, la mappa di ripristino può specificare un subset dei database da ripristinare.

*crstfilemap*

Numero di voci nel parametro della matrice *rgrstmap* .

*szBackupLogPath*

Percorso della directory in cui vengono ripristinati i file di log. Si tratta dei log che sono stati letti durante la sequenza di backup esterna. Questo percorso può essere uguale a quello di *szLogPath*.

*pLogInfo*

*PLogInfo* descrive diversi aspetti dei log di backup da ripristinare. questo parametro consente a **JetExternalRestore2** di prendere i parametri *genLow* e *genHigh* espliciti che **JetExternalRestore2** possiede, nonché il nome del log di base, anziché un presunto nome di base del log "edb".

*szTargetInstanceName*

Questo parametro è deprecato e non può essere utilizzato nell'applicazione.

*szTargetInstanceLogPath*

Percorso per i log di rollforward se il percorso dei log di cui si desidera eseguire il rollforward si trova in un set di registrazioni attivo o in un'istanza di. Questa operazione non deve essere specificata se l'istanza di destinazione usa la registrazione circolare.

*szTargetInstanceCheckpointPath*

Percorso del checkpoint durante il ripristino se non è presente alcuna istanza attiva in esecuzione in questa destinazione. Questa operazione non deve essere specificata se l'istanza di destinazione usa la registrazione circolare.

*PFN*

Callback di stato che segnala lo stato di avanzamento del ripristino.

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
<td><p>JET_errBadRestoreTargetInstance</p></td>
<td><p>Il <em>szTargetInstanceLogPath</em> specificato non appartiene a un'istanza inizializzata. Questo errore verrà restituito solo in Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseCorrupted</p></td>
<td><p>Indica che il database è danneggiato o un file non riconosciuto.</p></td>
</tr>
<tr class="even">
<td><p>JET_errEndingRestoreLogTooLow</p></td>
<td><p>Questo errore viene restituito se uno per i file di log in <em>szBackupLogPath</em>ha una generazione di log precedente a quella specificata in <em>genHigh</em> o <em>pLogInfo. ulGenHigh</em>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>L'operazione non è riuscita perché non è stato possibile aprire il file richiesto perché non è stato trovato nel percorso specificato.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro. Questo problema può verificarsi per <a href="gg294088(v=exchg.10).md">JetExternalRestore</a>e così via quando <em>szTargetCheckpointPath</em> e <em>szTargetInstanceLogPath</em> non sono entrambi specificati o non sono entrambi specificati. Ovvero devono corrispondere ed essere specificati o entrambi non specificati.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>L'operazione non è riuscita perché non è stato possibile trovare il percorso specificato.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per il completamento.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreOfNonBackupDatabase</p></td>
<td><p>Questo errore viene restituito se il file di database specificato durante l'operazione di ripristino non è un database di cui è stato eseguito il backup con backup esterno.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>Il motore di database non è in grado di eseguire il ripristino esterno o il ripristino a freddo in modalità istanza singola. Questo errore verrà restituito solo in Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errStartingRestoreLogTooHigh</p></td>
<td><p>Questo errore viene restituito se uno dei file di log in <em>szBackupLogPath</em>ha una generazione di log inferiore a quella specificata da <em>genLow</em> o <em>pLogInfo. ulGenLow</em>.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, tutti i database del *rgrstmap* vengono completamente ripristinati e in uno stato pulito o coerente. A questo punto è possibile rimontare il database in un'istanza esistente.

In caso di errore, il motore non è riuscito a recuperare il database. Il database è in uno stato non valido e, per ritentare il ripristino, è necessario ripristinare nuovamente l'intero database. In genere, l'origine di tale situazione è il danneggiamento del disco o del log, o un altro tipo di errore di gestione dei log oppure un set di log non continuo.

#### <a name="remarks"></a>Commenti

Vedere [JetExternalRestore](./jetexternalrestore-function.md).

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008 o Windows Server 2003.</p></td>
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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JetExternalRestore2W</strong> (Unicode) e <strong>JetExternalRestore2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetExternalRestore](./jetexternalrestore-function.md)  
[JetInit](./jetinit-function.md)
