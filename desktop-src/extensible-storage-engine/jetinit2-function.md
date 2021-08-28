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
ms.openlocfilehash: 7874c475dc18beb5d7f6849b9f628ea06cbc32a3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470456"
---
# <a name="jetinit2-function"></a>Funzione JetInit2


_**Si applica a:** Windows | Windows Server_

## <a name="jetinit2-function"></a>Funzione JetInit2

La **funzione JetInit2** inserisce il motore di database in uno stato in cui può supportare l'uso di file di database da parte dell'applicazione. Il motore deve essere già configurato correttamente per l'inizializzazione [tramite JetSetSystemParameter.](./jetsetsystemparameter-function.md) Il ripristino dell'arresto anomalo del database viene eseguito automaticamente come parte del processo di inizializzazione.

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

Per Windows 2000, questo parametro viene ignorato e deve sempre essere NULL.

Per Windows XP e versioni successive, l'uso di questo parametro dipende dalla modalità operativa del motore. Se il motore funziona in modalità legacy (modalità di compatibilità Windows 2000) in cui è supportata una sola istanza, questo parametro può essere NULL oppure può essere impostato su un buffer di output valido contenente NULL o JET_instanceNil che restituisce l'handle di istanza globale creato come effetto collaterale dell'inizializzazione. Questo handle di istanza può quindi essere passato a qualsiasi altra API che accetta un'istanza di . Se il motore funziona in modalità a istanze multipla, questo parametro deve essere impostato su un buffer di input valido contenente l'handle di istanza restituito da [JetCreateInstance](./jetcreateinstance-function.md) in fase di inizializzazione.

*grbit*

Gruppo di bit che specifica zero o più delle opzioni seguenti.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitReplayReplicatedLogFiles</p> | <p>Riservato per utilizzi futuri.</p> | 
| <p>JET_bitCreateSFSVolumeIfNotExist</p> | <p>Riservato per utilizzi futuri.</p> | 
| <p>JET_bitReplayIgnoreMissingDB</p> | <p>Questa opzione consente all'utente di eseguire il ripristino in un set di file di log, senza che tutti i database fossero presenti, collegati a un punto del set di log.</p> | 
| <p>JET_bitRecoveryWithoutUndo</p> | <p>Eseguire il ripristino, ma arrestarsi nella fase di annullamento. In questo modo è possibile copiare e applicare log delle transazioni aggiuntivi.</p> | 
| <p>JET_bitTruncateLogsAfterRecovery</p> | <p>In caso di ripristino soft riuscito, troncare i file di log.</p> | 
| <p>JET_bitReplayMissingMapEntryDB</p> | <p>La voce della mappa di database mancante viene per impostazione predefinita nella stessa posizione.</p> | 
| <p>JET_bitReplayIgnoreLostLogs</p> | <p>Ignorare i log persi dalla fine del flusso di log.</p><p><strong>Windows 7:JET_bitReplayIgnoreLostLogs</strong> è stato introdotto in Windows 7.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


#### <a name="remarks"></a>Commenti

Un'istanza deve essere inizializzata con una chiamata a **JetInit2** prima di poter essere usata da un oggetto diverso da [JetSetSystemParameter.](./jetsetsystemparameter-function.md)

Un'istanza viene distrutta da una chiamata alla [funzione JetTerm,](./jetterm-function.md) anche se tale istanza non è mai stata inizializzata usando [JetInit](./jetinit-function.md). Un'istanza è l'unità di recuperabilità per il motore di database. Controlla il ciclo di vita di tutti i file usati per proteggere l'integrità dei dati in un set di file di database. Questi file includono il file di checkpoint e i file di log delle transazioni.

Se il ripristino è in esecuzione in un set di log, per il quale non sono presenti tutti i database (che restituiranno il JET_errAttachedDatabaseMismatch di errore in circostanze normali) e il client desidera che il ripristino continui nonostante i database mancanti, viene usato bitReplayIgnoreMissingDB di JET_ per continuare il ripristino per i database disponibili.

Per altre informazioni, vedere la sezione Osservazioni in [JetInit.](./jetinit-function.md)

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[File del motore Archiviazione estendibile](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit3](./jetinit3-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parametri delle risorse](./resource-parameters.md)
