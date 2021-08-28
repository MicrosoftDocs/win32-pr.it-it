---
description: 'Altre informazioni su: Funzione JetExternalRestore'
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
ms.openlocfilehash: 480a3411152f1388bee0115ecbcffc88f6ded09b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984854"
---
# <a name="jetexternalrestore-function"></a>Funzione JetExternalRestore


_**Si applica a:** Windows | Windows Server_

## <a name="jetexternalrestore-function"></a>Funzione JetExternalRestore

La **funzione JetExternalRestore** ripristina un backup esterno eseguito con le API di backup esterne e specifica un intervallo di numeri di file di log da riprodurre durante il processo di ripristino. Questo processo è noto come ripristino a hard, che è simile ma diverso dal recupero a tempo indeterminato eseguito dalla [funzione JetInit.](./jetinit-function.md)

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

Si tratta di una matrice [JET_RSTMAP](./jet-rstmap-structure.md) strutture . Si tratta di una mappa di percorsi o nomi file di database nuovi e vecchi. Viene usato perché potrebbe essere necessario ripristinare i database in un percorso diverso da quello da cui è stato eseguito il backup. Nel caso in cui più database siano collegati a un singolo set di registrazione, la mappa di ripristino può specificare un subset di database da ripristinare.

*crstfilemap*

Numero di voci nel parametro *di matrice rgrstmap.*

*szBackupLogPath*

Percorso della directory in cui vengono ripristinati i file di log. Si tratta dei log letti durante la sequenza di backup esterna. Questo percorso può essere lo stesso di szLogPath.

*genLow*

Il numero di file di log più basso che deve essere riprodotto da *szBackupLogPath*. La fedeltà completa di un valore long senza segno deve essere mantenuta, ma nelle versioni correnti del motore questo numero è un numero esadecimale compreso nell'intervallo 0x00000 a 0xFFFFF. Questo potrebbe cambiare nelle versioni future.

*genHigh*

Numero di file di log più alto da riprodurre da *szBackupLogPath*. La fedeltà completa di un valore long senza segno deve essere mantenuta, ma nelle versioni correnti del motore questo numero è un numero esadecimale compreso nell'intervallo 0x00000 a 0xFFFFF. Questo potrebbe cambiare nelle versioni future.

*Pfn*

Callback di stato, per segnalare lo stato di avanzamento del ripristino.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errOutOfMemory</p> | <p>L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per completarla.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro. Questa operazione può verificarsi per <strong>JetExternalRestore</strong>e così via quando <em>szTargetCheckpointPath</em> e <em>szTargetInstanceLogPath</em> non sono entrambi specificati o non sono entrambi non specificati. In altri casi, devono corrispondere ed essere entrambi specificati o entrambi non specificati.</p> | 
| <p>JET_errDatabaseCorrupted</p> | <p>Ciò indica che il database è danneggiato o un file non riconosciuto.</p> | 
| <p>JET_errFileNotFound</p> | <p>L'operazione non è riuscita perché non è stato possibile aprire il file richiesto perché non è stato trovato nel percorso specificato.</p> | 
| <p>JET_errInvalidPath</p> | <p>L'operazione non è riuscita perché non è stato possibile trovare il percorso specificato.</p> | 
| <p>JET_errRestoreOfNonBackupDatabase</p> | <p>Questo errore viene restituito se il file di database specificato durante il ripristino non è un database di cui è stato eseguito il backup esterno.</p> | 
| <p>JET_errStartingRestoreLogTooHigh</p> | <p>Questo errore viene restituito se uno dei file di log in <em>szBackupLogPath</em>ha una generazione di log inferiore a quella specificata da <em>genLow</em> o <em>pLogInfo.ulGenLow.</em></p> | 
| <p>JET_errEndingRestoreLogTooLow</p> | <p>Questo errore viene restituito se uno dei file di log in <em>szBackupLogPath</em>ha una generazione di log superiore a quella specificata in <em>genHigh</em> o <em>pLogInfo.ulGenHigh</em>.</p> | 
| <p>JET_errBadRestoreTargetInstance</p> | <p>Il <em>valore szTargetInstanceLogPath</em> specificato non appartiene a un'istanza inizializzata. Questo errore verrà restituito solo in Windows XP e versioni successive.</p> | 
| <p>JET_errRunningInOneInstanceMode</p> | <p>Il motore di database non può eseguire il ripristino esterno o il ripristino a disco rigido in modalità istanza singola. Questo errore verrà restituito solo in Windows XP e versioni successive.</p> | 



In caso di esito positivo, tutti i database di *rgrstmap* vengono ripristinati completamente e in uno stato pulito o coerente. A questo punto il database può essere rimontato in un'istanza esistente.

In caso di errore, il motore non è riuscito a recuperare il database. Il database è in uno stato non valido e per ritentare il ripristino a prova l'intero database deve essere ripristinato nuovamente. In genere, l'origine di una situazione di questo tipo è il danneggiamento del disco o del log o un'altra forma di gestione errata del log o un set di log non continuo.

#### <a name="remarks"></a>Commenti

Per comprendere il funzionamento di un ripristino "rigido", è necessario comprendere che esistono tre fasi di ripristino e che la seconda fase può avere due parti. Nella fase I i log sono necessari per garantire la coerenza di un database di cui è stato eseguito il backup (oppure è possibile usare un set iniziale di log incrementali). Nella fase II vengono utilizzati tutti i log di roll forward aggiuntivi disponibili per rendere coerente il database. È anche disponibile una riproduzione dei log di roll forward aggiuntivi. La fase III è la fase di annullamento del ripristino.

Fase I: viene eseguita la riproduzione del set di log che deve essere ripristinato per portare il database a uno stato coerente (o un set iniziale di file di log). In pratica, si tratta della riproduzione del set di file di log che non sono facoltativi per i database da ripristinare. Se mancano log in questo intervallo di log, il ripristino avrà esito negativo. Questi log devono essere inseriti nella directory specificata nel *parametro szBackupLogPath.*

Fase II: facoltativamente, alcuni set di file di log possono essere file di log di roll forward provenienti da backup incrementali o differenziali e dai file di log di un'istanza attiva. Nel caso di file di log da backup incrementali o differenziali, i file di log possono essere inseriti nelle directory specificate nei parametri *szBackupLogPath* o *szTargetInstanceLogPath,* con la prima directory consigliata. I log usati per la fase di roll forward (fase II) devono derivare dalla stessa serie di log riprodotti durante la fase I e devono avere numeri di log a incremento continuo senza gap dai log della fase I. Per riprodurre un database completamente aggiornato con i file di log attualmente usati da un'istanza attiva, è necessario specificare i parametri *szTargetInstanceLogPath* e *szTargetInstanceCheckpointPath.* Questa operazione può essere eseguita anche mentre altri database sono collegati a tale set di log.

Fase III: nella fase finale del ripristino viene eseguito il rollback di tutte le transazioni di cui non è stato eseguito il commit, che richiede la generazione di nuovi file di log e l'aggiornamento del file di checkpoint. Questa fase viene talvolta definita "annullamento". Il percorso del file di checkpoint da usare durante questa fase è il percorso analogo al percorso del log della fase III, ad esempio se si usa *szLogPath* per la fase III, verrà usato *szCheckpointFilePath,* se si usa *szTargetInstanceLogPath* per la fase III del ripristino *szTargetInstanceCheckpointPath.*

Per comprendere il funzionamento dei percorsi, usare questo diagramma di flusso:

![ESE_Documentation_ese1](images/Gg294088.ESE_Documentation_ese1(EXCHG.10).gif "ESE_Documentation_ese1")

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetExternalRestoreW</strong> (Unicode) e <strong>JetExternalRestoreA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetInit](./jetinit-function.md)
