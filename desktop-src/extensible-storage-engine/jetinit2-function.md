---
description: 'Altre informazioni su: Funzione JetInit2'
title: Funzione JetInit2
TOCTitle: JetInit2 Function
ms:assetid: b5541429-6ce6-457b-88cf-673d267f6209
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294065(v=EXCHG.10)
ms:contentKeyID: 32765680
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit2
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9b5d2a62aa448a84d539d8d2d557d06befacfbba
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988954"
---
# <a name="jetinit2-function"></a>Funzione JetInit2


_**Si applica a:** Windows | Windows Server_

## <a name="jetinit2-function"></a>Funzione JetInit2

La **funzione JetInit2 inserisce** il motore di database in uno stato in cui può supportare l'uso di file di database da parte dell'applicazione. Il motore deve essere già configurato correttamente per l'inizializzazione [tramite JetSetSystemParameter.](./jetsetsystemparameter-function.md) Il recupero da un arresto anomalo del database viene eseguito automaticamente come parte del processo di inizializzazione.

**Windows XP:****JetInit2** è stato introdotto in Windows XP.  

questa funzione è obsoleta. In [alternativa, usare JetInit3.](./jetinit3-function.md)

```cpp
JET_ERR JET_API JetInit2(
  __in_out_opt  JET_INSTANCE* pinstance,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parametri

*pinstance*

Istanza di da utilizzare per questa chiamata.

Per Windows 2000, questo parametro viene ignorato e deve essere sempre NULL.

Per Windows XP e versioni successive, l'uso di questo parametro dipende dalla modalità operativa del motore. Se il motore funziona in modalità legacy (modalità di compatibilità Windows 2000) in cui è supportata una sola istanza, questo parametro può essere NULL oppure può essere impostato su un buffer di output valido contenente NULL o JET_instanceNil che restituisce l'handle di istanza globale creato come effetto collaterale dell'inizializzazione. Questo handle di istanza può quindi essere passato a qualsiasi altra API che accetta un'istanza di . Se il motore opera in modalità a istanza multipla, questo parametro deve essere impostato su un buffer di input valido contenente l'handle di istanza restituito dall'istanza [jetCreateInstance](./jetcreateinstance-function.md) da inizializzare.

*grbit*

Gruppo di bit che specifica zero o più delle opzioni seguenti.


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitReplayReplicatedLogFiles</p> | <p>Riservato per utilizzi futuri.</p> | 
| <p>JET_bitCreateSFSVolumeIfNotExist</p> | <p>Riservato per utilizzi futuri.</p> | 
| <p>JET_bitReplayIgnoreMissingDB</p> | <p>Questa opzione consente all'utente di eseguire il ripristino su un set di file di log, senza che tutti i database fossero presenti, collegati in un punto del set di log.</p> | 
| <p>JET_bitRecoveryWithoutUndo</p> | <p>Eseguire il ripristino, ma interrompersi in fase di annullamento. Ciò consente la copia e l'applicazione di log delle transazioni aggiuntivi.</p> | 
| <p>JET_bitTruncateLogsAfterRecovery</p> | <p>In caso di esito positivo del ripristino ammoramento, troncare i file di log.</p> | 
| <p>JET_bitReplayMissingMapEntryDB</p> | <p>Voce della mappa di database mancante per impostazione predefinita nella stessa posizione.</p> | 
| <p>JET_bitReplayIgnoreLostLogs</p> | <p>Ignorare i log persi dalla fine del flusso di log.</p><p><strong>Windows 7:JET_bitReplayIgnoreLostLogs</strong> è stato introdotto in Windows 7.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


#### <a name="remarks"></a>Commenti

Un'istanza deve essere inizializzata con una chiamata a **JetInit2** prima di poter essere usata da qualsiasi elemento diverso da [JetSetSystemParameter.](./jetsetsystemparameter-function.md)

Un'istanza viene distrutta da una chiamata alla [funzione JetTerm,](./jetterm-function.md) anche se tale istanza non è mai stata inizializzata usando [JetInit.](./jetinit-function.md) Un'istanza è l'unità di recuperabilità per il motore di database. Controlla il ciclo di vita di tutti i file usati per proteggere l'integrità dei dati in un set di file di database. Questi file includono il file del checkpoint e i file di log delle transazioni.

Se il ripristino è in esecuzione in un set di log, per il quale non sono presenti tutti i database (che restituirà l'errore JET_errAttachedDatabaseMismatch in circostanze normali) e il client vuole che il ripristino continui nonostante i database mancanti, il database JET_ bitReplayIgnoreMissingDB viene usato per continuare il ripristino per i database disponibili.

Per altre informazioni, vedere la sezione Osservazioni in [JetInit.](./jetinit-function.md)

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[Extensible Archiviazione Engine Files](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit3](./jetinit3-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parametri delle risorse](./resource-parameters.md)
