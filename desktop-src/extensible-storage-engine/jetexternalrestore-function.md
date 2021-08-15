---
description: Altre informazioni sulla funzione JetExternalRestore
title: Funzione JetExternalRestore
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
ms.openlocfilehash: 4844c14d6b60e5825b3b09f58b0d756e83b0f41c4e743684a29607a814d4f16f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118072825"
---
# <a name="jetexternalrestore-function"></a>Funzione JetExternalRestore


_**Si applica a:** Windows | Windows Server_

## <a name="jetexternalrestore-function"></a>Funzione JetExternalRestore

La **funzione JetExternalRestore** ripristina un backup esterno eseguito con le API di backup esterne e specifica un intervallo di numeri di file di log da riprodurre durante il processo di ripristino. Questo è noto come ripristino rigido, che è simile ma diverso dal ripristino soft eseguito dalla [funzione JetInit.](./jetinit-function.md)

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

Percorso del file del checkpoint da usare durante il ripristino se *szTargetInstanceCheckpointPath* non è specificato o dispone già di un'istanza attiva o in esecuzione.

*szLogPath*

Percorso o directory per i log per la fase finale (annullamento) del ripristino ed eventualmente per i log di roll forward. Questo percorso può essere lo stesso di *szBackupLogPath*.

*rgrstmap*

Si tratta di una matrice [di JET_RSTMAP](./jet-rstmap-structure.md) struttura. Si tratta di una mappa di percorsi o nomi di file di database vecchi e nuovi. Viene usato perché potrebbe essere necessario ripristinare i database in un percorso diverso da quello da cui è stato eseguito il backup. Nel caso in cui più database siano collegati a un singolo set di registrazione, la mappa di ripristino può specificare un subset di database da ripristinare.

*crstfilemap*

Numero di voci nel parametro della matrice *rgrstmap.*

*szBackupLogPath*

Percorso della directory in cui vengono ripristinati i file di log. Si tratta dei log letti durante la sequenza di backup esterna. Questo percorso può essere lo stesso di szLogPath.

*genLow*

Numero di file di log più basso da riprodurre da *szBackupLogPath*. La fedeltà completa di un valore long senza segno deve essere mantenuta, ma nelle versioni correnti del motore questo numero è un numero esadecimale nell'intervallo compreso tra 0x00000 a 0xFFFFF. Questo potrebbe cambiare nelle versioni future.

*genHigh*

Numero di file di log più alto che deve essere riprodotto da *szBackupLogPath*. La fedeltà completa di un valore long senza segno deve essere mantenuta, ma nelle versioni correnti del motore questo numero è un numero esadecimale nell'intervallo compreso tra 0x00000 a 0xFFFFF. Questo potrebbe cambiare nelle versioni future.

*Pfn*

Callback di stato, per segnalare lo stato del ripristino.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Errori del motore Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).

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
<td><p>L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per completarla.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti conteneva un valore imprevisto o conteneva un valore che non aveva senso se combinato con il valore di un altro parametro. Ciò può verificarsi per <strong>JetExternalRestore</strong>e così via quando <em>szTargetCheckpointPath</em> e <em>szTargetInstanceLogPath</em> non sono entrambi specificati o non entrambi non specificati. In altri casi, devono corrispondere ed essere entrambi specificati o entrambi non specificati.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseCorrupted</p></td>
<td><p>Ciò indica che il database è stato danneggiato o un file non riconosciuto.</p></td>
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
<td><p>Questo errore viene restituito se il file di database specificato durante il ripristino non è un database di cui è stato eseguito il backup esterno.</p></td>
</tr>
<tr class="even">
<td><p>JET_errStartingRestoreLogTooHigh</p></td>
<td><p>Questo errore viene restituito se uno dei file di log in <em>szBackupLogPath</em>ha una generazione di log inferiore a quella specificata da <em>genLow</em> o <em>pLogInfo.ulGenLow</em>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errEndingRestoreLogTooLow</p></td>
<td><p>Questo errore viene restituito se uno dei file di log in <em>szBackupLogPath</em>ha una generazione di log superiore a quella specificata in <em>genHigh</em> o <em>pLogInfo.ulGenHigh</em>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadRestoreTargetInstance</p></td>
<td><p><em>SzTargetInstanceLogPath specificato</em> non appartiene a un'istanza inizializzata. Questo errore verrà restituito solo in Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>Il motore di database non può eseguire il ripristino esterno o il ripristino rigido in modalità a istanza singola. Questo errore verrà restituito solo in Windows XP e versioni successive.</p></td>
</tr>
</tbody>
</table>


In caso di esito positivo, tutti i database di *rgrstmap* vengono completamente ripristinati e in uno stato pulito o coerente. A questo punto il database può essere rimontaggio in un'istanza esistente.

In caso di errore, il motore non è riuscito a ripristinare il database. Il database è in uno stato non valido e per ritentare il ripristino rigido è necessario ripristinare nuovamente l'intero database. In genere, l'origine di una situazione di questo tipo è il danneggiamento del disco o del log o un'altra forma di gestione errata del log o un set di log non continuo.

#### <a name="remarks"></a>Commenti

Per comprendere il funzionamento di un ripristino "rigido", è necessario comprendere che esistono tre fasi di ripristino e che la seconda fase può avere due parti. Nella fase I, i log sono necessari per garantire la coerenza di un database di cui è stato eseguito il backup oppure è possibile usare un set iniziale di log incrementali. Nella fase II vengono utilizzati tutti i log di roll forward aggiuntivi disponibili per rendere coerente il database. È anche disponibile una riproduzione dei log di roll forward aggiuntivi. La fase III è la fase di annullamento del ripristino.

Fase I: viene eseguita la riproduzione del set di log che deve essere ripristinato per portare il database a uno stato coerente (o un set iniziale di file di log). In pratica, si tratta della riproduzione del set di file di log che non sono facoltativi per i database da ripristinare. Se sono presenti log mancanti da questo intervallo di log, il ripristino avrà esito negativo. Questi log devono essere inseriti nella directory specificata nel *parametro szBackupLogPath.*

Fase II: facoltativamente, possono essere presenti alcuni set di file di log che sono file di log di roll forward provenienti da backup incrementali o differenziali e dai file di log di un'istanza attiva. Nel caso di file di log da backup incrementali o differenziali, i file di log possono essere inseriti nelle directory specificate nei parametri *szBackupLogPath* o *szTargetInstanceLogPath,* con la prima directory consigliata. I log usati per la fase di roll forward (fase II) devono derivare dalla stessa serie di log riprodotti durante la fase I e devono avere numeri di log a incremento continuo senza lacune dai log di fase I. Per riprodurre un database completamente aggiornato con i file di log attualmente usati da un'istanza attiva, è necessario specificare i parametri *szTargetInstanceLogPath* e *szTargetInstanceCheckpointPath.* Questa operazione può essere eseguita anche quando altri database sono collegati a tale set di log.

Fase III: nella fase finale del ripristino viene eseguito il rollback di tutte le transazioni di cui non è stato eseguito il commit, che richiede la generazione di nuovi file di log e l'aggiornamento del file del checkpoint. Questa fase viene talvolta definita "annullamento". Il percorso del file del checkpoint da usare durante questa fase è il percorso analogo al percorso del log di fase III, ad esempio se *szLogPath* viene usato per la fase III, verrà usato *szCheckpointFilePath,* se *szTargetInstanceLogPath* viene usato per la fase III di ripristino *szTargetInstanceCheckpointPath.*

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
<td><p>Dichiarato in Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Libreria</strong></p></td>
<td><p>Usare ESENT.lib.</p></td>
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
