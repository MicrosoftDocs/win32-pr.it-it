---
description: Altre informazioni sulla funzione JetDupCursor
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
ms.openlocfilehash: 009b84837895ce13f63cc37e4b5b152f4274ee62
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985884"
---
# <a name="jetdupcursor-function"></a>Funzione JetDupCursor


_**Si applica a:** Windows | Windows Server_

## <a name="jetdupcursor-function"></a>Funzione JetDupCursor

La **funzione JetDupCursor** duplica un cursore aperto e restituisce un handle per il cursore duplicato. Se il cursore duplicato era un cursore di sola lettura, anche il cursore duplicato è un cursore di sola lettura. Qualsiasi stato correlato alla costruzione di una chiave di ricerca o all'aggiornamento di un record non viene copiato nel cursore duplicato. Inoltre, la posizione del cursore originale non viene duplicata nel cursore duplicato. Il cursore duplicato viene sempre aperto nell'indice cluster e la relativa posizione è sempre sulla prima riga della tabella.

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

Puntatore a *tableid*.

*grbit*

Riservato per utilizzi futuri.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore di Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errOutOfCursors</p> | <p>Non esistono risorse cursore disponibili.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



In caso di esito positivo, *ptableid* viene impostato su un cursore duplicato.

In caso di errore, non vengono apportate modifiche. Lo stato *di tableid* rimane invariato.

#### <a name="remarks"></a>Commenti

Il cursore duplicato non ha l'intero stato del cursore copiato. La posizione del cursore duplicato, incluso l'indice corrente, è in genere diversa dal cursore specificato. Il cursore duplicato viene sempre restituito sull'indice cluster e sulla prima riga della tabella. Se la tabella è vuota, il cursore duplicato non si trova in alcuna riga.

Le tabelle aperte **con JetDupCursor** devono in genere essere chiuse con [JetCloseTable](./jetclosetable-function.md). L'eccezione a questa regola si verifica quando **jetDupCursor** viene chiamato in una transazione e viene eseguito il rollback della transazione (con [JetRollback](./jetrollback-function.md)). Quando si esegue il rollback di una transazione, il cursore viene chiuso automaticamente. In questo caso, è un errore chiudere la tabella con [JetCloseTable](./jetclosetable-function.md).

Il numero di tabelle che è possibile aprire contemporaneamente è influenzato direttamente da [JET_paramMaxOpenTables](./resource-parameters.md). Per [informazioni dettagliate, vedere Parametri](./extensible-storage-engine-system-parameters.md) di sistema.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
