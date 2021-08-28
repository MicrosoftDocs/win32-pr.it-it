---
description: Altre informazioni sulla funzione JetBeginSession
title: Funzione JetBeginSession
TOCTitle: JetBeginSession Function
ms:assetid: f1c33b78-f2d1-44ea-8ec9-94b729b94e24
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294131(v=EXCHG.10)
ms:contentKeyID: 32765745
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginSessionA
- JetBeginSession
- JetBeginSessionW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e6263916211e5d21e0032ba6de8d98e46fedfa9
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989074"
---
# <a name="jetbeginsession-function"></a>Funzione JetBeginSession


_**Si applica a:** Windows | Windows Server_

## <a name="jetbeginsession-function"></a>Funzione JetBeginSession

La **funzione JetBeginSession** avvia una sessione e inizializza e restituisce un handle di sessione ESE ([JET_SESID](./jet-sesid.md)). Le sessioni controllano tutti gli accessi al database e vengono utilizzate per controllare l'ambito delle transazioni. La sessione può essere utilizzata per avviare, eseguire il commit o interrompere le transazioni. La sessione viene usata anche per collegare, creare o aprire un database. La sessione viene usata come contesto per tutte le operazioni DDL e DML. Per aumentare la concorrenza e l'accesso parallelo al database, è possibile iniziare più sessioni.

```cpp
    JET_ERR JET_API JetBeginSession(
      __in          JET_INSTANCE instance,
      __out         JET_SESID* psesid,
      __in_opt      JET_PCSTR szUserName,
      __in_opt      JET_PCSTR szPassword
    );
```

### <a name="parameters"></a>Parametri

*Istanza*

Istanza del database da utilizzare per questa chiamata.

*psesid*

Puntatore alla variabile inizializzata dall'handle di sessione al completamento della restituzione.

*szUserName*

Questo parametro è riservato.

*szPassword*

Questo parametro è riservato.

### <a name="return-value"></a>Valore restituito

Questa funzione consente la restituzione di [tutti JET_ERR](./jet-err.md)definiti in questa API. Per altre informazioni sugli errori Jet, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errOutOfMemory</p> | <p>L'operazione non è riuscita perché non è stato possibile allocare memoria.</p> | 
| <p>JET_errOutOfSessions</p> | <p>Il numero di sessioni che il motore consentirà l'avvio del client è limitato. Questo valore può essere modificato usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter con</a> la JET_paramMaxSessions costante. Il numero predefinito di sessioni è 16. Vedere <a href="gg294139(v=exchg.10).md">Parametri di sistema</a> per informazioni dettagliate JET_paramMaxSessions.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



In caso di esito positivo, l'handle di sessione viene inizializzato e può essere usato per le operazioni di database.

In caso di errore, non sono disponibili sessioni o non è stato possibile inizializzare una nuova sessione.

#### <a name="remarks"></a>Commenti

Quando si usano sessioni tra thread diversi, è necessario prestare attenzione. Una sessione tiene traccia del thread in cui è stato usato durante [JetBeginTransaction,](./jetbegintransaction-function.md) [JetCommitTransaction](./jetcommittransaction-function.md)o [JetRollback](./jetrollback-function.md)e genera un errore se usato in più thread con una transazione aperta. [JetResetSessionContext,](./jetresetsessioncontext-function.md) [JetSetSessionContext](./jetsetsessioncontext-function.md) può modificare questo comportamento. Poiché la sessione è ancora un contesto serializzato e non è possibile eseguire contemporaneamente più operazioni di database su una singola sessione, solo in serie. Tuttavia, è possibile usare più sessioni per ottenere l'accesso simultaneo al database. Le sessioni possono essere usate all'interno di una transazione tra thread impostando e reimpostando i contesti di sessione.

L'handle di sessione deve essere chiuso [con JetEndSession.](./jetendsession-function.md)

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetBeginSessionW</strong> (Unicode) e <strong>JetBeginSessionA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[Sessione JetDupSession](./jetdupsession-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSessionContext](./jetsetsessioncontext-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
