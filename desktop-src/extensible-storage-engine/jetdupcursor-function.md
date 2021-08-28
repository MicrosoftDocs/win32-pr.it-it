---
description: 'Altre informazioni su: Funzione JetDupCursor'
title: Funzione JetDupCursor
TOCTitle: JetDupCursor Function
ms:assetid: 154b7d2d-4656-46b3-873c-2e194a9059b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269193(v=EXCHG.10)
ms:contentKeyID: 32765496
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupCursor
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a96f93357bc3df143fa63ed690295e40980cfc94
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472657"
---
# <a name="jetdupcursor-function"></a>Funzione JetDupCursor


_**Si applica a:** Windows | Windows Server_

## <a name="jetdupcursor-function"></a>Funzione JetDupCursor

La **funzione JetDupCursor** duplica un cursore aperto e restituisce un handle al cursore duplicato. Se il cursore duplicato è un cursore di sola lettura, anche il cursore duplicato è un cursore di sola lettura. Qualsiasi stato correlato alla costruzione di una chiave di ricerca o all'aggiornamento di un record non viene copiato nel cursore duplicato. Inoltre, la posizione del cursore originale non viene duplicata nel cursore duplicato. Il cursore duplicato viene sempre aperto nell'indice cluster e la relativa posizione è sempre sulla prima riga della tabella.

```cpp
    JET_ERR JET_API JetDupCursor(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_TABLEID* ptableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableid*

Cursore da utilizzare per questa chiamata.

*ptableid*

Puntatore *a tableid*.

*grbit*

Riservato per utilizzi futuri.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errOutOfCursors</p> | <p>Non esistono risorse cursore disponibili.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



In caso di esito *positivo, ptableid* viene impostato su un cursore duplicato.

In caso di errore, non vengono apportate modifiche. Lo stato di *tableid* rimane invariato.

#### <a name="remarks"></a>Commenti

Per il cursore duplicato non viene copiato l'intero stato del cursore. La posizione del cursore duplicato, incluso l'indice corrente, è in genere diversa dal cursore specificato. Il cursore duplicato viene sempre restituito sull'indice cluster e sulla prima riga della tabella. Se la tabella è vuota, il cursore duplicato non si trova in alcuna riga.

Le tabelle aperte **con JetDupCursor** devono in genere essere chiuse [con JetCloseTable.](./jetclosetable-function.md) L'eccezione a questa regola si verifica quando **JetDupCursor** viene chiamato in una transazione e viene eseguito il rollback della transazione (con [JetRollback](./jetrollback-function.md)). Quando si esegue il rollback di una transazione, il cursore viene chiuso automaticamente. In questo caso, è un errore chiudere la tabella con [JetCloseTable](./jetclosetable-function.md).

Il numero di tabelle che possono essere aperte simultaneamente è influenzato direttamente da [JET_paramMaxOpenTables](./resource-parameters.md). Per [informazioni dettagliate, vedere](./extensible-storage-engine-system-parameters.md) Parametri di sistema.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
