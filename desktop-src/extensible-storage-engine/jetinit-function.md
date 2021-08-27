---
description: 'Altre informazioni su: Funzione JetInit'
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
ms.openlocfilehash: d074e07dec88bf0b33ec56b1391986758fbd388c
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984534"
---
# <a name="jetinit-function"></a>Funzione JetInit


_**Si applica a:** Windows | Windows Server_

## <a name="jetinit-function"></a>Funzione JetInit

La **funzione JetInit** inserisce il motore di database in uno stato in cui può supportare l'uso dei file di database da parte dell'applicazione. Il motore deve essere già configurato correttamente per l'inizializzazione [tramite JetSetSystemParameter.](./jetsetsystemparameter-function.md) Il recupero da un arresto anomalo del database viene eseguito automaticamente come parte del processo di inizializzazione.

```cpp
JET_ERR JET_API JetInit(
  __in_out_opt  JET_INSTANCE* pinstance
);
```

### <a name="parameters"></a>Parametri

*pinstance*

Istanza di da utilizzare per questa chiamata.

Per Windows 2000, questo parametro viene ignorato e deve essere sempre NULL.

Per Windows XP e versioni successive, l'uso di questo parametro dipende dalla modalità operativa del motore. Se il motore funziona in modalità legacy (modalità di compatibilità Windows 2000) in cui è supportata una sola istanza, questo parametro può essere NULL oppure può essere impostato su un buffer di output valido che restituirà l'handle di istanza globale creato come effetto collaterale dell'inizializzazione. Questo buffer di output deve essere impostato su NULL o JET_instanceNil. Questo handle di istanza può quindi essere passato a qualsiasi altra funzione che usa un'istanza di . Se il motore funziona in modalità a istanza multipla, questo parametro deve essere impostato su un buffer di input valido che contiene l'handle di istanza restituito dall'istanza della funzione [JetCreateInstance](./jetcreateinstance-function.md) in fase di inizializzazione.


#### <a name="remarks"></a>Commenti

Un'istanza deve essere inizializzata con una chiamata a **JetInit** prima di poter essere usata da qualsiasi elemento diverso da [JetSetSystemParameter.](./jetsetsystemparameter-function.md)

Un'istanza viene distrutta da una chiamata alla [funzione JetTerm,](./jetterm-function.md) anche se tale istanza non è mai stata inizializzata usando **JetInit.** Un'istanza è l'unità di recuperabilità per il motore di database. Controlla il ciclo di vita di tutti i file usati per proteggere l'integrità dei dati in un set di file di database. Questi file includono il file del checkpoint e i file di log delle transazioni.

Il numero massimo di istanze che possono essere create contemporaneamente è controllato da [JET_paramMaxInstances](./resource-parameters.md), che può essere configurato da una chiamata a [JetSetSystemParameter.](./jetsetsystemparameter-function.md) Quando il motore di database viene inizializzato per la prima volta, **JetInit** creerà un set iniziale di file per supportare tale istanza. Questi file includono un file del checkpoint (denominato \<[JET_paramBaseName](./transaction-log-parameters.md)\> . CHK), un set di file di log delle transazioni riservati (denominato RES1. LOG e RES2. LOG), un file di log delle transazioni iniziale (denominato \<[JET_paramBaseName](./transaction-log-parameters.md)\> . LOG) e un file di database temporaneo (denominato in base [JET_paramTempPath](./temporary-database-parameters.md)). Se [JET_paramRecovery](./transaction-log-parameters.md) è impostato su "Off", il file del checkpoint e i file di log non verranno creati. Se [JET_paramMaxTemporaryTables](./temporary-database-parameters.md) è impostato su zero, il file di database temporaneo non verrà creato. Questi file rappresentano il footprint su disco di un'istanza di e devono essere gestiti con cautela. Se questi file sono danneggiati singolarmente o l'uno rispetto all'altro, i dati archiviati nei database associati all'istanza potrebbero andare persi.

Quando il motore di database viene inizializzato con un set esistente di file di log delle transazioni, tali file verranno esaminati per verificare se l'operazione precedente dell'istanza ha subito un arresto anomalo. Se viene rilevato un arresto anomalo del sistema, verrà eseguito automaticamente il ripristino dall'arresto anomalo del sistema. Questo processo ricostruirà i database collegati all'istanza durante l'operazione precedente del motore e salverà di nuovo le modifiche nei file di database. Il risultato sarà un database coerente con le transazioni. Questo processo può richiedere molto tempo se il numero di file di log delle transazioni da riprodurre nei database è elevato.

A causa del fatto che **JetInit** esegue il ripristino in caso di arresto anomalo del sistema, è possibile che quasi tutti gli errori del motore di database siano restituiti in caso di errore. In pratica, la maggior parte degli errori rilevati nella distribuzione rientra in due categorie: danneggiamento dei dati e gestione errata dei file. Il danneggiamento dei dati si manifesterà più spesso negli errori seguenti o simili:

  - Jet_errreadverifyfailure

  - JET_errLogFileCorrupt

  - JET_errCheckpointCorrupt

Questi errori sono quasi sempre causati da problemi hardware e pertanto non possono essere evitati. La gestione errata dei file si manifesterà più spesso negli errori seguenti o simili:

  - JET_errMissingLogFile

  - JET_errAttachedDatabaseMismatch

  - JET_errDatabaseSharingViolation

  - JET_errInvalidLogSequence

Se il ripristino è in esecuzione in un set di log, per il quale non sono presenti tutti i database (che restituirà il JET_errAttachedDatabaseMismatch di errore in circostanze normali) e il client desidera che il ripristino continui nonostante i database mancanti, è possibile usare bitReplayIgnoreMissingDB di JET_ per continuare il ripristino per i database disponibili. Questi errori sono evitabili dall'applicazione. L'applicazione deve prestare attenzione a proteggere il repository di questi file dalla manipolazione da forza esterne, ad esempio l'utente o altre applicazioni. Se l'applicazione vuole eliminare completamente un'istanza, è necessario eliminare tutti i file associati all'istanza. Sono inclusi il file del checkpoint, i file di log delle transazioni e tutti i file di database collegati all'istanza.

La **funzione JetInit** si comporta in modo diverso, rispetto ai file di database collegati all'istanza, tra Windows 2000 e versioni successive.

**Windows 2000:**  In Windows 2000, qualsiasi database collegato all'istanza durante un'operazione precedente di tale istanza rimane collegato all'istanza dopo il corretto completamento **di JetInit.** Non è necessario chiamare [JetAttachDatabase](./jetattachdatabase-function.md) dopo **JetInit** per assicurare l'accesso successivo al database. Se la [funzione JetAttachDatabase](./jetattachdatabase-function.md) viene chiamata dopo la **funzione JetInit,** JET_wrnDatabaseAttached verrà restituito l'avviso. Questo avviso indica che l'allegato del database è stato mantenuto e può essere ignorato.

**Windows XP:**  In Windows XP e versioni successive, tutti i database vengono scollegati automaticamente dall'istanza da **JetInit.** Questo significa che [JetAttachDatabase](./jetattachdatabase-function.md) deve essere sempre chiamato dopo **JetInit** in questo caso.

Qualsiasi applicazione scritta per l'esecuzione Windows 2000 e versioni successive deve sempre chiamare [JetAttachDatabase](./jetattachdatabase-function.md) dopo **JetInit.** Se l'applicazione viene eseguita in Windows 2000, in alcuni casi deve prevedere JET_wrnDatabaseAttached'applicazione. Per [altre informazioni, vedere JetAttachDatabase.](./jetattachdatabase-function.md)

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[File extensible Archiviazione Engine](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_paramMaxTemporaryTables](./temporary-database-parameters.md)  
[JET_paramRecovery](./transaction-log-parameters.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit3](./jetinit3-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
