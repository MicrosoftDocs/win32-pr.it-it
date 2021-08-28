---
description: Altre informazioni sulla funzione JetGetRecordSize2
title: Funzione JetGetRecordSize2
TOCTitle: JetGetRecordSize2 Function
ms:assetid: 803cfb4e-44f3-447a-b642-018e6f2f713f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269314(v=EXCHG.10)
ms:contentKeyID: 32765604
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordSize2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 68c503192f0be157a59e8e3b32c817231f35e25c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478297"
---
# <a name="jetgetrecordsize2-function"></a>Funzione JetGetRecordSize2


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetrecordsize2-function"></a>Funzione JetGetRecordSize2

La **funzione JetGetRecordSize2** recupera le informazioni sulle dimensioni dei record dalla posizione desiderata.

**Windows 7: JetGetRecordSize2** è stato introdotto nel sistema operativo Windows 7.

```cpp
    JET_ERR JET_API JetGetRecordSize2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECSIZE2* precsize,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Identifica il contesto della sessione di database che verrà usato per la chiamata API.

*tableid*

Identifica la tabella o il cursore che verrà usato per la chiamata API. Il cursore deve essere posizionato su un record o deve essere preparato un aggiornamento.

*precsize*

Puntatore a un buffer di output per la [JET_RECSIZE2](./jet-recsize2-structure.md) struttura .

*grbit*

Si tratta di uno o più dei valori seguenti.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitRecordSizeInCopyBuffer</p> | <p>In questo modo vengono recuperate le dimensioni del record che si trova nel buffer di copia preparato per l'aggiornamento. In caso contrario, il cursore o <em>tableid</em> deve essere posizionato in un record e verrà usato tale record.</p> | 
| <p>JET_bitRecordSizeRunningTotal</p> | <p>Quando questo bit viene specificato, il <a href="gg269174(v=exchg.10).md">JET_RECSIZE2</a> non viene azzerato prima di compilare il contenuto, fungendo di fatto da accumulo delle statistiche per più record visitati o aggiornati.</p> | 
| <p>JET_bitRecordSizeLocal</p> | <p>In questo modo l'API ignora i valori Long non intrinseci. Ad esempio, verrà usato solo il record locale nella pagina.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>Una delle opzioni richieste non è valida o non è implementata. Questo errore verrà restituito dalla <strong>funzione JetGetRecordSize2</strong> quando viene specificato <em>un grbit</em> non valido.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è stata inizializzata.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p><strong>Windows XP:</strong> JET_errInstanceUnavailable verrà restituito solo dal sistema operativo Windows XP e dalle versioni successive di Windows.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Non è valido usare la stessa sessione per più thread contemporaneamente.</p><p><strong>Windows XP:</strong> JET_errInstanceUnavailable verrà restituito solo da Windows XP e versioni successive di Windows.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Questa situazione può verificarsi se il cursore è stato posizionato in modo non corretto.</p> | 
| <p>JET_errRecordDeleted</p> | <p>Se il cursore non è stato posizionato in una transazione, questa situazione può verificarsi se un altro thread elimina il record da in questa sessione.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Può essere restituito se è <strong>stata passata</strong><em>una precsize</em> NULL.</p> | 



#### <a name="remarks"></a>Commenti

Le dimensioni della chiave accumulata nel campo **cbOverhead** di [JET_RECSIZE2](./jet-recsize2-structure.md), è influenzata da JET_bitRecordSizeInCopyBuffer. Se questo bit viene specificato, le dimensioni della chiave accumulate nel **campo cbOverhead** sono le dimensioni complete della chiave. Se questo bit non viene usato, le dimensioni della chiave accumulate non includeranno le dimensioni salvate a causa della compressione del prefisso della chiave.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_RECSIZE](./jet-recsize-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)
