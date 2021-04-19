---
description: 'Altre informazioni su: funzione JetGetCursorInfo'
title: JetGetCursorInfo (funzione)
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
ms.openlocfilehash: 7201c37f79f68deead837cdcdd90402e4b2bf1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319633"
---
# <a name="jetgetcursorinfo-function"></a>JetGetCursorInfo (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetcursorinfo-function"></a>JetGetCursorInfo (funzione)

La funzione **JetGetCursorInfo** viene utilizzata per determinare se un aggiornamento del record corrente di un cursore provocherà un conflitto di scrittura, in base allo stato corrente dell'aggiornamento del record. È possibile che venga restituito un conflitto di scrittura anche se **JetGetCursorInfo** restituisce JET_errSuccess, perché un'altra sessione può aggiornare il record prima che la sessione corrente sia in grado di aggiornare lo stesso record.

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

Sessione che verrà utilizzata per questa chiamata.

*TableID*

Cursore che verrà utilizzato per la chiamata.

*pvResult*

Riservato per utilizzi futuri.

*cbMax*

Deve essere impostato su 0 (zero); in caso contrario, non utilizzato. È presente per le funzionalità future.

*InfoLevel*

Deve essere impostato su 0 (zero); in caso contrario, non utilizzato. È presente per le funzionalità future.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti. Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .

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
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p><em>CbMax</em> è diverso da 0 (zero) o <em>InfoLevel</em> non è 0 (zero).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Il cursore non si trova attualmente in un record e le informazioni su un record logico non possono essere restituite come risultato.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione per più di un thread nello stesso momento. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errWriteConflict</p></td>
<td><p>Il record corrente del cursore è stato aggiornato da un'altra sessione e un aggiornamento del record da questa sessione provocherà un conflitto di scrittura.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, questa operazione non ha alcun effetto sulla posizione del cursore, ma indica che non è attualmente stato aggiornato da nessun'altra sessione.

In caso di errore, se viene restituito un codice di errore negativo non sono presenti effetti sul cursore o sul database.

#### <a name="remarks"></a>Commenti

Questa operazione non influisce sullo stato del cursore o dei dati. Restituisce solo un codice di errore che indica se un aggiornamento del record corrente da parte della sessione chiamante è noto come risultato di un JET_errWriteConflict o è sconosciuto per restituire JET_errWriteConflict. Se il record è già stato aggiornato da un'altra sessione per utilizzarlo, è certo che un aggiornamento del record da questa sessione provocherà un conflitto di scrittura. Questa operazione sarà valida fino a quando questa sessione non eseguirà il commit o il rollback delle transazioni a livello di transazione 0 (zero). Tuttavia, se **JetGetCursorInfo** restituisce JET_errSuccess, è ancora possibile che un'altra sessione aggiorni questo record prima della sessione corrente e quindi è comunque possibile che un aggiornamento del record corrente da questa sessione nella transazione corrente provochi un conflitto di scrittura.

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
<td><p>Dichiarata in esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Libreria</strong></p></td>
<td><p>Usare ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Richiede ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetLock](./jetgetlock-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetUpdate](./jetupdate-function.md)
