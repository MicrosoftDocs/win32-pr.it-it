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
ms.openlocfilehash: 0852de04f3969e3e30debc7ba7ff4f3aedf7ac4084b17f91feed8984fe4e1467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118251615"
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

Questa funzione consente la restituzione di [qualsiasi JET_ERR](./jet-err.md)definiti in questa API. Per altre informazioni sugli errori Jet, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Codice restituito</p></th>
<th><p>Descrizione</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Operazione riuscita.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p>
<p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>L'operazione non è riuscita perché non è stato possibile allocare memoria.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfSessions</p></td>
<td><p>Il numero di sessioni che il motore consentirà l'avvio del client è limitato. Questo valore può essere modificato usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter con</a> la JET_paramMaxSessions costante. Il numero predefinito di sessioni è 16. Vedere <a href="gg294139(v=exchg.10).md">Parametri di sistema</a> per informazioni dettagliate JET_paramMaxSessions.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p></td>
</tr>
</tbody>
</table>


In caso di esito positivo, l'handle di sessione viene inizializzato e può essere usato per le operazioni di database.

In caso di errore, non sono disponibili sessioni o non è stato possibile inizializzare una nuova sessione.

#### <a name="remarks"></a>Commenti

Quando si usano sessioni tra thread diversi, è necessario prestare attenzione. Una sessione tiene traccia del thread in cui è stato usato durante [JetBeginTransaction,](./jetbegintransaction-function.md) [JetCommitTransaction](./jetcommittransaction-function.md)o [JetRollback](./jetrollback-function.md)e genera un errore se usato in più thread con una transazione aperta. [JetResetSessionContext,](./jetresetsessioncontext-function.md) [JetSetSessionContext](./jetsetsessioncontext-function.md) può modificare questo comportamento. Poiché la sessione è ancora un contesto serializzato e non è possibile eseguire contemporaneamente più operazioni di database su una singola sessione, solo in serie. Tuttavia, è possibile usare più sessioni per ottenere l'accesso simultaneo al database. Le sessioni possono essere usate all'interno di una transazione tra thread impostando e reimpostando i contesti di sessione.

L'handle di sessione deve essere chiuso [con JetEndSession.](./jetendsession-function.md)

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarato in Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Libreria</strong></p></td>
<td><p>Usare ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Richiede ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JetBeginSessionW</strong> (Unicode) e <strong>JetBeginSessionA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


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
