---
description: 'Altre informazioni su: funzione JetExternalRestore'
title: JetExternalRestore (funzione)
TOCTitle: JetExternalRestore Function
ms:assetid: c930689a-3ea6-4c5a-9318-76f519f23343
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294088(v=EXCHG.10)
ms:contentKeyID: 32765703
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetExternalRestoreA
- JetExternalRestore
- JetExternalRestoreW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 087949817ac0bcbe2effe2ff136a6ce80084daa2
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323807"
---
# <a name="jetexternalrestore-function"></a>JetExternalRestore (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetexternalrestore-function"></a>JetExternalRestore (funzione)

La funzione **JetExternalRestore** ripristina un backup esterno che è stato eseguito con le API di backup esterne e specifica un intervallo di numeri di file di log da riprodurre durante il processo di ripristino. Questa operazione è nota come ripristino a livello di hardware, che è simile a, ma diverso dal ripristino soft come eseguito dalla funzione [JetInit](./jetinit-function.md) .

```cpp
JET_ERR JET_API JetExternalRestore(
  __in          JET_PSTR szCheckpointFilePath,
  __in          JET_PSTR szLogPath,
  __in_opt      JET_RSTMAP* rgrstmap,
  __in          long crstfilemap,
  __in          JET_PSTR szBackupLogPath,
  __in          long genLow,
  __in          long genHigh,
  __in          JET_PFNSTATUS pfn
);
```

### <a name="parameters"></a>Parametri

*szCheckpointFilePath*

Percorso del file del checkpoint da utilizzare durante il ripristino se *szTargetInstanceCheckpointPath* non è specificato o è già presente un'istanza attiva o in esecuzione.

*szLogPath*

Percorso o directory dei log per la fase finale (annullamento) del ripristino ed eventualmente per i log di rollforward. Questo percorso può essere uguale a quello di *szBackupLogPath*.

*rgrstmap*

Si tratta di una matrice di strutture di [JET_RSTMAP](./jet-rstmap-structure.md) . Si tratta di una mappa di percorsi di database vecchi e nuovi o di nomi file. Questa operazione viene utilizzata perché potrebbe essere necessario ripristinare i database in un percorso diverso da quello di cui è stato eseguito il backup. Nel caso in cui più database siano collegati a un singolo set di registrazione, la mappa di ripristino può specificare un subset di database da ripristinare.

*crstfilemap*

Numero di voci nel parametro della matrice *rgrstmap* .

*szBackupLogPath*

Percorso della directory in cui vengono ripristinati i file di log. Si tratta dei log che sono stati letti durante la sequenza di backup esterna. Questo percorso può essere uguale a quello di szLogPath.

*genLow*

Numero di file di log più basso che deve essere riprodotto da *szBackupLogPath*. È necessario mantenere la fedeltà completa di un long senza segno, ma nelle versioni correnti del motore questo numero è un numero esadecimale compreso nell'intervallo tra 0x00000 e 0xFFFFF. Questo può cambiare nelle versioni future.

*genHigh*

Numero massimo di file di log che deve essere riprodotto da *szBackupLogPath*. È necessario mantenere la fedeltà completa di un long senza segno, ma nelle versioni correnti del motore questo numero è un numero esadecimale compreso nell'intervallo tra 0x00000 e 0xFFFFF. Questo può cambiare nelle versioni future.

*PFN*

Callback di stato per segnalare lo stato di avanzamento del ripristino.

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
<td><p>JET_errOutOfMemory</p></td>
<td><p>L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per il completamento.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro. Questo problema può verificarsi per <strong>JetExternalRestore</strong>e così via quando <em>szTargetCheckpointPath</em> e <em>szTargetInstanceLogPath</em> non sono entrambi specificati o non sono entrambi specificati. Ovvero devono corrispondere ed essere specificati o entrambi non specificati.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseCorrupted</p></td>
<td><p>Indica che il database è danneggiato o un file non riconosciuto.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>L'operazione non è riuscita perché non è stato possibile aprire il file richiesto perché non è stato trovato nel percorso specificato.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPath</p></td>
<td><p>L'operazione non è riuscita perché non è stato possibile trovare il percorso specificato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreOfNonBackupDatabase</p></td>
<td><p>Questo errore viene restituito se il file di database specificato durante l'operazione di ripristino non è un database di cui è stato eseguito il backup con backup esterno.</p></td>
</tr>
<tr class="even">
<td><p>JET_errStartingRestoreLogTooHigh</p></td>
<td><p>Questo errore viene restituito se uno dei file di log in <em>szBackupLogPath</em>ha una generazione di log inferiore a quella specificata da <em>genLow</em> o <em>pLogInfo. ulGenLow</em>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errEndingRestoreLogTooLow</p></td>
<td><p>Questo errore viene restituito se uno per i file di log in <em>szBackupLogPath</em>ha una generazione di log precedente a quella specificata in <em>genHigh</em> o <em>pLogInfo. ulGenHigh</em>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadRestoreTargetInstance</p></td>
<td><p>Il <em>szTargetInstanceLogPath</em> specificato non appartiene a un'istanza inizializzata. Questo errore verrà restituito solo in Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>Il motore di database non è in grado di eseguire il ripristino esterno o il ripristino a freddo in modalità istanza singola. Questo errore verrà restituito solo in Windows XP e versioni successive.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, tutti i database del *rgrstmap* vengono completamente ripristinati e in uno stato pulito o coerente. A questo punto è possibile rimontare il database in un'istanza esistente.

In caso di errore, il motore non è riuscito a recuperare il database. Il database è in uno stato non valido e, per ritentare il ripristino, è necessario ripristinare nuovamente l'intero database. In genere, l'origine di tale situazione è il danneggiamento del disco o del log, o un altro tipo di errore di gestione dei log oppure un set di log non continuo.

#### <a name="remarks"></a>Commenti

Per comprendere il funzionamento di un ripristino "complesso", è necessario comprendere che esistono tre fasi di ripristino e la seconda fase può avere due parti. Nella fase I, I log sono obbligatori a garantire la coerenza di un database di cui è stato eseguito il backup (oppure è possibile usare un set iniziale di log incrementali). Nella fase II vengono utilizzati tutti i log di rollforward aggiuntivi disponibili per rendere il database coerente. È inoltre disponibile una riproduzione dei log di rollforward aggiuntivi. La fase III è la fase di rollback del ripristino.

Fase I: viene eseguita la riproduzione del set di log che deve essere ripristinato per portare il database a uno stato coerente (o a un set di file di log iniziale). In sostanza, si tratta della riproduzione del set di file di log non facoltativi per i database da ripristinare. Se sono presenti log mancanti da questo intervallo di log, il ripristino avrà esito negativo. Questi log devono essere inseriti nella directory specificata nel parametro *szBackupLogPath* .

Fase II: facoltativamente, possono essere presenti alcuni set di file di log che eseguono il rollforward dei file di log che provengono da backup incrementali o differenziali e dai file di log di un'istanza attiva. Nel caso di file di log di backup incrementali o differenziali, i file di log possono essere inseriti nelle directory specificate nei parametri *szBackupLogPath* o *szTargetInstanceLogPath* , con il primo che è la directory consigliata. I log usati per la fase di rollforward (fase II) dovrebbero provenire dalla stessa serie di log rilasciati durante la fase I e devono avere incrementato continuamente I numeri di log senza gap dalla fase I log. Per riprodurre un database in modo che sia completamente aggiornato con i file di log attualmente utilizzati da un'istanza attiva, è necessario specificare i parametri *szTargetInstanceLogPath* e *szTargetInstanceCheckpointPath* . Questa operazione può essere eseguita anche mentre altri database sono collegati a tale set di log.

Fase III: nella fase finale del ripristino, viene eseguito il rollback di tutte le transazioni di cui non è stato eseguito il commit, che richiedono la generazione di nuovi file di log e l'aggiornamento del file del checkpoint. Questa fase viene a volte definita "annullamento". Il percorso del file del checkpoint da usare durante questa fase è il percorso analogo al percorso del log della fase III, ovvero se *szLogPath* viene usato per la fase III, viene usato *szCheckpointFilePath* se viene usato *szTargetInstanceLogPath* per la fase III del ripristino *szTargetInstanceCheckpointPath* .

Per comprendere il funzionamento dei percorsi, usare questo diagramma di flusso:

![ESE_Documentation_ese1](images/Gg294088.ESE_Documentation_ese1(EXCHG.10).gif "ESE_Documentation_ese1")

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JetExternalRestoreW</strong> (Unicode) e <strong>JetExternalRestoreA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetInit](./jetinit-function.md)
