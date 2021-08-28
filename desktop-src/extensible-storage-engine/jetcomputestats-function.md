---
description: 'Altre informazioni su: Funzione JetComputeStats'
title: Funzione JetComputeStats
TOCTitle: JetComputeStats Function
ms:assetid: 142f6ab0-715f-493a-a762-7a83854498d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269192(v=EXCHG.10)
ms:contentKeyID: 32765495
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetComputeStats
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d990e4ded7dc2485bec6b5ecf92d9999aad57ce5
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122981974"
---
# <a name="jetcomputestats-function"></a>Funzione JetComputeStats


_**Si applica a:** Windows | Windows Server_

## <a name="jetcomputestats-function"></a>Funzione JetComputeStats

La **funzione JetComputeStats** illustra ogni indice di una tabella per calcolare esattamente il numero di voci in un indice e il numero di chiavi distinte in un indice. Queste informazioni, insieme al numero di pagine di database allocate per un indice e all'ora corrente del calcolo, vengono archiviate nei metadati dell'indice nel database. Questi dati possono essere successivamente recuperati con operazioni di informazioni.

```cpp
    JET_ERR JET_API JetComputeStats(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableid*

Cursore che verrà utilizzato per questa chiamata. Descrive la tabella su cui calcolare le statistiche.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errRollbackError</p> | <p>Si è verificato un errore che richiede l'esecuzione del rollback di tutte le modifiche, ma il rollback della transazione non è riuscito.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente.</p><p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



In caso di esito positivo, le statistiche aggiornate vengono archiviate nei cataloghi di database per la tabella descritta con il cursore specificato.

In caso di errore, non viene effettuato alcun aggiornamento di alcun tipo al database.

#### <a name="remarks"></a>Commenti

Questa operazione può richiedere un utilizzo di risorse, perché ogni indice in una tabella deve essere visto per intero. [JetGetRecordPosition](./jetgetrecordposition-function.md) può essere usato per ottenere una stima approssimativa del numero di voci in un indice, ma non può stimare di per sé il numero di valori distinti in un indice.

I dati calcolati da questa operazione iniziano a diventare non aggiornati e la tabella viene successivamente aggiornata.

Gli aggiornamenti al database apportati **da JetComputeStats** vengono evasi in modalità differita. Ciò significa che non verrà eseguita alcuna operazione di scaricamento del log e un arresto anomalo del sistema in seguito a un ritorno di JET_errSuccess da parte di **JetComputeStats** può comunque causare la perdita di questi aggiornamenti.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_SESID](./jet-sesid.md)  
[JetGetRecordPosition](./jetgetrecordposition-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetStopService](./jetstopservice-function.md)
