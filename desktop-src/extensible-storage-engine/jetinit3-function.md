---
description: 'Altre informazioni su: Funzione JetInit3'
title: Funzione JetInit3
TOCTitle: JetInit3 Function
ms:assetid: 752589b6-1b8f-4b6f-a14a-00f4b1405db5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269296(v=EXCHG.10)
ms:contentKeyID: 32765588
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit3
- JetInit3A
- JetInit3W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a0c73343550768a9ccd061c702fae89d562d095
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477907"
---
# <a name="jetinit3-function"></a>Funzione JetInit3


_**Si applica a:** Windows | Windows Server_

## <a name="jetinit3-function"></a>Funzione JetInit3

La **funzione JetInit3 inserisce** il motore di database in uno stato in cui può supportare l'uso dei file di database da parte dell'applicazione. Il motore deve essere già configurato correttamente per l'inizializzazione, operazione eseguita tramite la [funzione JetSetSystemParameter.](./jetsetsystemparameter-function.md) Si noti che il recupero dall'arresto anomalo del database viene eseguito automaticamente come parte del processo di inizializzazione.

**Windows Vista:****JetInit3** è stato introdotto in Windows Vista.  

```cpp
    JET_ERR JET_API JetInit3(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in_opt      JET_RSTINFO* prstInfo,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*pinstance*

Istanza di utilizzata per una chiamata specifica. L'utilizzo di questo parametro dipende dalla modalità operativa del motore. Se il motore funziona in modalità legacy (modalità di compatibilità Windows 2000), in cui è supportata una sola istanza, è possibile impostare questo parametro su **NULL** o su un buffer di output valido contenente **NULL** o JET_instanceNil, che restituisce l'handle di istanza globale creato come effetto collaterale dell'inizializzazione. Questo handle di istanza può quindi essere passato a qualsiasi altra API che accetta un'istanza di . Se il motore opera in modalità a istanza multipla, è necessario impostare questo parametro su un buffer di input valido contenente l'handle di istanza restituito dalla funzione [JetCreateInstance](./jetcreateinstance-function.md) in fase di inizializzazione.

*prstInfo*

Parametri di ripristino aggiuntivi usati per modificare il mapping dei database durante il ripristino, per impostare la posizione in cui il ripristino verrà interrotta o per determinare lo stato di ripristino corrente.

*grbit*

Gruppo di bit che specifica zero o più opzioni elencate e definite nella tabella seguente.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitReplayReplicatedLogFiles</p> | <p>Questo valore è riservato per l'uso futuro.</p> | 
| <p>JET_bitCreateSFSVolumeIfNotExist</p> | <p>Questo valore è riservato per l'uso futuro.</p> | 
| <p>JET_bitReplayIgnoreMissingDB</p> | <p>Questo valore consente all'utente di eseguire il ripristino su un set di file di log, anche in assenza dei database collegati al file di log impostato a un certo punto.</p> | 
| <p>JET_bitRecoveryWithoutUndo</p> | <p>Questo valore consente all'utente di eseguire il ripristino, ma solo fino alla fase di annullamento(e non includendo). Usando questo valore, è possibile copiare e applicare log delle transazioni aggiuntivi.</p> | 
| <p>JET_bitTruncateLogsAfterRecovery</p> | <p>Questo valore determina il troncamento dei file di log durante un recupero a tempo in corso.</p> | 
| <p>JET_bitReplayMissingMapEntryDB</p> | <p>Questo valore determina l'impostazione predefinita di una voce di mapping del database mancante nella stessa posizione.</p> | 
| <p>JET_bitReplayIgnoreLostLogs</p> | <p>Questo valore fa sì che i log persi dalla fine del flusso di log vengono ignorati durante un ripristino.</p><p><strong>Windows 7:JET_bitReplayIgnoreLostLogs</strong> è stato introdotto in Windows 7.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE [(Extensible](./extensible-storage-engine-errors.md) Archiviazione Engine), vedere Extensible Archiviazione Engine Errors and [Error Handling Parameters](./error-handling-parameters.md).


#### <a name="remarks"></a>Commenti

Un'istanza deve essere inizializzata con una chiamata alla funzione **JetInit3** prima che possa essere usata da qualsiasi elemento diverso dalla [funzione JetSetSystemParameter.](./jetsetsystemparameter-function.md)

Un'istanza viene distrutta da una chiamata alla [funzione JetTerm,](./jetterm-function.md) anche se tale istanza non è mai stata inizializzata usando la [funzione JetInit.](./jetinit-function.md) Un'istanza è l'unità di recuperabilità per il motore di database. Controlla il ciclo di vita di tutti i file usati per proteggere l'integrità dei dati in un set di file di database. Questi file includono il file del checkpoint e i file di log delle transazioni. Si noti che [JetTerm](./jetterm-function.md) non deve essere chiamato se la **funzione JetInit3** ha esito negativo. Tuttavia, [JetTerm deve](./jetterm-function.md) comunque essere chiamato per tutte le istanze create da **JetCreateInstance2** se **JetInit3** non è mai stato chiamato o **se JetInit3** ha esito positivo.

Se il ripristino è in esecuzione in un set di log per cui non sono presenti tutti i database correlati (che restituirà l'errore JET_errAttachedDatabaseMismatch in circostanze normali) e il client vuole che il ripristino continui nonostante i database mancanti, l'errore di JET_bitReplayIgnoreMissingDB viene usato per continuare il ripristino per i database disponibili.

Poiché il ripristino da arresto anomalo del sistema in genere non avviene nello stesso computer (e con la stessa configurazione) del momento dell'arresto anomalo, un database in genere non cambia posizione. In alcuni scenari, ad esempio lo spostamento di file in un computer diverso o il ripristino del backup di snapshot in posizioni diverse, questo non è più vero. La **funzione JetInit3** consente di specificare un mapping (usando le strutture [JET_RSTINFO](./jet-rstinfo-structure.md) e [JET_RSTMAP)](./jet-rstmap-structure.md) tra la posizione precedente del database e la nuova posizione. In realtà, è necessario solo il nuovo percorso, purché i file di database siano presenti in tale percorso. Non appena si conoscono i percorsi dei database ripristinati, la firma del database verrà usata per identificare il database tramite il processo di ripristino. Sarà necessario il percorso del database originale solo se è necessario creare nuovamente un database, nel qual caso la firma è nota.

Inoltre, se è necessario arrestare un ripristino dopo un'operazione di annullamento, è possibile specificare una posizione del log specifica in cui il ripristino verrà interrotta. Si noti che ciò include la possibilità di arrestarsi alla fine di una determinata generazione di log se la posizione specificata fa parte della generazione ma oltre la fine del log effettivo.

Per altre informazioni, vedere la sezione "Osservazioni" [nell'argomento JetInit.](./jetinit-function.md)

#### <a name="requirements"></a>Requisiti


| | | <p>Client</p> | <p>Richiede Windows Vista.</p> | | <p>Server</p> | <p>Richiede Windows Server 2008.</p> | | <p>Intestazione</p> | <p>Dichiarato in Esent.h.</p> | | <p>Libreria</p> | <p>Usa ESENT.lib.</p> | | <p>DLL</p> | <p>Richiede ESENT.dll.</p> | | <p>Unicode</p> | <p>Implementato come <strong>JetInit3W</strong> (Unicode) e <strong>JetInit3A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[Extensible Archiviazione Engine Files](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_RSTINFO](./jet-rstinfo-structure.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parametri delle risorse](./resource-parameters.md)
