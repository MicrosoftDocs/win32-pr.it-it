---
description: Altre informazioni sulla funzione JetGetCursorInfo
title: Funzione JetGetCursorInfo
TOCTitle: JetGetCursorInfo Function
ms:assetid: e779fa5d-1d7e-46f1-80c9-f7c819279188
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294126(v=EXCHG.10)
ms:contentKeyID: 32765740
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCursorInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e6c26aa69f1ac51cdd9d70ca93c4fc42df5356ee
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987664"
---
# <a name="jetgetcursorinfo-function"></a>Funzione JetGetCursorInfo


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetcursorinfo-function"></a>Funzione JetGetCursorInfo

La **funzione JetGetCursorInfo** viene usata per determinare se un aggiornamento del record corrente di un cursore genererà un conflitto di scrittura, in base allo stato di aggiornamento corrente del record. È possibile che alla fine venga restituito un conflitto di scrittura anche se **JetGetCursorInfo** restituisce JET_errSuccess, perché un'altra sessione può aggiornare il record prima che la sessione corrente sia in grado di aggiornare lo stesso record.

```cpp
    JET_ERR JET_API JetGetCursorInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione che verrà usata per questa chiamata.

*tableid*

Cursore che verrà usato per questa chiamata.

*pvResult*

Riservato per utilizzi futuri.

*cbMax*

Deve essere impostato su 0 (zero), in caso contrario non usato. È presente per funzionalità future.

*InfoLevel*

Deve essere impostato su 0 (zero), in caso contrario non usato. È presente per funzionalità future.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore di Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidParameter</p> | <p><em>cbMax non</em> è 0 (zero) o <em>InfoLevel</em> non è 0 (zero).</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Il cursore non è attualmente in un record e le informazioni su un record logico non possono essere restituite di conseguenza.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p>JET_errWriteConflict</p> | <p>Il record corrente del cursore è stato aggiornato da un'altra sessione e un aggiornamento di questo record da parte di questa sessione comporta un conflitto di scrittura.</p> | 



In caso di esito positivo, questa operazione non ha alcun effetto sulla posizione del cursore, ma indica solo che nessun'altra sessione ha attualmente aggiornato questo record.

In caso di errore, se viene restituito un codice di errore negativo, il cursore o il database non ha alcun effetto.

#### <a name="remarks"></a>Commenti

Questa operazione non influisce sullo stato del cursore o dei dati. Restituisce solo un codice di errore che indica se è noto che un aggiornamento al record corrente da parte della sessione chiamante ha come risultato un JET_errWriteConflict o è sconosciuto per restituire JET_errWriteConflict. Se un'altra sessione ha già aggiornato questo record per usarlo, è certo che un aggiornamento di questo record da parte di questa sessione comporta un conflitto di scrittura. Ciò sarà vero fino a quando questa sessione non esegue il commit o il rollback delle transazioni a livello di transazione 0 (zero). Tuttavia, se **JetGetCursorInfo** restituisce JET_errSuccess, è comunque possibile che un'altra sessione aggiornerà questo record prima della sessione corrente e pertanto è comunque possibile che un aggiornamento del record corrente da parte di questa sessione nella transazione corrente restituisca un conflitto di scrittura.

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
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetLock](./jetgetlock-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetUpdate](./jetupdate-function.md)
