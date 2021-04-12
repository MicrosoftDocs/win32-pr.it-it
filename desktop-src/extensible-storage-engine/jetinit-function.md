---
description: 'Altre informazioni su: funzione JetInit'
title: Funzione JetInit
TOCTitle: JetInit Function
ms:assetid: b7f78cca-7268-4045-bda2-20746b1d6370
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294068(v=EXCHG.10)
ms:contentKeyID: 32765683
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 308c012bc5eb144e0ac0d608c64d63ccf39aeca1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104356214"
---
# <a name="jetinit-function"></a>Funzione JetInit


_**Si applica a:** Windows | Windows Server_

## <a name="jetinit-function"></a>Funzione JetInit

La funzione **JetInit** inserisce il motore di database in uno stato in cui può supportare l'utilizzo di file di database da parte dell'applicazione. Il motore deve essere già configurato correttamente per l'inizializzazione tramite [JetSetSystemParameter](./jetsetsystemparameter-function.md). Il ripristino dell'arresto anomalo del database viene eseguito automaticamente nell'ambito del processo di inizializzazione.

```cpp
JET_ERR JET_API JetInit(
  __in_out_opt  JET_INSTANCE* pinstance
);
```

### <a name="parameters"></a>Parametri

*pinstance*

Istanza di da utilizzare per questa chiamata.

Per Windows 2000, questo parametro viene ignorato e deve essere sempre NULL.

Per Windows XP e versioni successive, l'uso di questo parametro dipende dalla modalità operativa del motore. Se il motore funziona in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza, questo parametro può essere NULL o può essere impostato su un buffer di output valido che restituirà l'handle dell'istanza globale creato come effetto collaterale dell'inizializzazione. Questo buffer di output deve essere impostato su NULL o JET_instanceNil. Questo handle di istanza può quindi essere passato a qualsiasi altra funzione che usa un'istanza di. Se il motore funziona in modalità a istanze diverse, questo parametro deve essere impostato su un buffer di input valido che contiene l'handle dell'istanza restituito dall'istanza della funzione [JetCreateInstance](./jetcreateinstance-function.md) che viene inizializzata.


#### <a name="remarks"></a>Commenti

Un'istanza deve essere inizializzata con una chiamata a **JetInit** prima che possa essere usata da un valore diverso da [JetSetSystemParameter](./jetsetsystemparameter-function.md).

Un'istanza viene distrutta da una chiamata alla funzione [JetTerm](./jetterm-function.md) , anche se tale istanza non è mai stata inizializzata usando **JetInit**. Un'istanza è l'unità di recupero per il motore di database. Consente di controllare il ciclo di vita di tutti i file utilizzati per proteggere l'integrità dei dati in un set di file di database. Questi file includono il file del checkpoint e i file di log delle transazioni.

Il numero massimo di istanze che è possibile creare in qualsiasi momento è controllato da [JET_paramMaxInstances](./resource-parameters.md), che può essere configurato tramite una chiamata a [JetSetSystemParameter](./jetsetsystemparameter-function.md). Quando il motore di database viene inizializzato per la prima volta, **JetInit** creerà un set iniziale di file per supportare tale istanza. Questi file includono un file del checkpoint (denominato \<[JET_paramBaseName](./transaction-log-parameters.md)\> . CHK), un set di file di log delle transazioni riservati, denominato RES1. LOG e RES2. LOG), un file di log delle transazioni iniziale, denominato \<[JET_paramBaseName](./transaction-log-parameters.md)\> . LOG) e un file di database temporaneo (denominato in base a [JET_paramTempPath](./temporary-database-parameters.md)). Se [JET_paramRecovery](./transaction-log-parameters.md) è impostato su "off", il file del checkpoint e i file di log non verranno creati. Se [JET_paramMaxTemporaryTables](./temporary-database-parameters.md) è impostato su zero, il file di database temporaneo non verrà creato. Questi file rappresentano l'impronta sul disco di un'istanza e devono essere gestiti con cautela. Se questi file sono danneggiati singolarmente o rispetto a un altro, i dati archiviati nei database associati all'istanza potrebbero andare persi.

Quando il motore di database viene inizializzato con un set di file di log delle transazioni esistente, questi file vengono controllati per verificare se l'incarnazione precedente dell'istanza è stata danneggiata. Se viene rilevato un arresto anomalo, il ripristino dell'arresto anomalo verrà eseguito automaticamente. Questo processo ricostruirà i database collegati all'istanza durante la precedente incarnazione del motore e salverà le modifiche nei file di database. Il risultato sarà costituito da database coerenti con le transazioni. Questo processo può richiedere molto tempo se il numero di file di log delle transazioni da riprodurre sui database è elevato.

A causa del fatto che **JetInit** esegue il ripristino dell'arresto anomalo del sistema, è possibile che venga restituito quasi qualsiasi errore del motore di database in caso di errore. In pratica, la maggior parte degli errori riscontrati nella distribuzione rientrano in due categorie: il danneggiamento dei dati e la gestione degli errori del file. Il danneggiamento dei dati si manifesterà più spesso negli errori seguenti o simili:

  - JET_errReadVerifyFailure

  - JET_errLogFileCorrupt

  - JET_errCheckpointCorrupt

Questi errori sono quasi sempre causati da problemi hardware e pertanto non possono essere evitati. La gestione non automatica dei file si manifesterà più spesso negli errori seguenti o simili:

  - JET_errMissingLogFile

  - JET_errAttachedDatabaseMismatch

  - JET_errDatabaseSharingViolation

  - JET_errInvalidLogSequence

Se il ripristino viene eseguito in un set di log, per cui non sono presenti tutti i database (che restituiscono l'errore JET_errAttachedDatabaseMismatch in circostanze normali) e il client desidera che il ripristino continui nonostante i database mancanti, è possibile utilizzare il JET_ bitReplayIgnoreMissingDB per continuare il ripristino dei database disponibili. Questi errori possono essere evitati dall'applicazione. L'applicazione deve prestare attenzione a proteggere il repository di questi file dalla manipolazione da parte di forze esterne, ad esempio l'utente o altre applicazioni. Se l'applicazione desidera eliminare completamente un'istanza, è necessario eliminare tutti i file associati all'istanza. Sono inclusi il file del checkpoint, i file di log delle transazioni e tutti i file di database collegati all'istanza.

La funzione **JetInit** si comporta in modo diverso rispetto ai file di database collegati all'istanza tra Windows 2000 e versioni successive.

**Windows 2000:**  In Windows 2000, qualsiasi database collegato all'istanza durante un'incarnazione precedente di tale istanza rimane collegato all'istanza dopo che **JetInit** è stato completato correttamente. Non è necessario chiamare [JetAttachDatabase](./jetattachdatabase-function.md) dopo **JetInit** per garantire l'accesso al database in un secondo momento. Se la funzione [JetAttachDatabase](./jetattachdatabase-function.md) viene chiamata dopo la funzione **JetInit** , verrà restituito il JET_wrnDatabaseAttached avviso. Questo avviso indica che l'allegato del database è stato mantenuto e può essere ignorato.

**Windows XP:**  In Windows XP e versioni successive, tutti i database vengono scollegati automaticamente dall'istanza di da **JetInit**. Ciò significa che [JetAttachDatabase](./jetattachdatabase-function.md) deve sempre essere chiamato dopo **JetInit** in questo caso.

Qualsiasi applicazione scritta per l'esecuzione in Windows 2000 e nelle versioni successive deve sempre chiamare [JetAttachDatabase](./jetattachdatabase-function.md) dopo **JetInit**. Se l'applicazione viene eseguita in Windows 2000, è necessario che venga visualizzata JET_wrnDatabaseAttached in alcuni casi. Per ulteriori informazioni, vedere [JetAttachDatabase](./jetattachdatabase-function.md) .

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

[File del motore di archiviazione estendibile](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_paramMaxTemporaryTables](./temporary-database-parameters.md)  
[JET_paramRecovery](./transaction-log-parameters.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit3](./jetinit3-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
