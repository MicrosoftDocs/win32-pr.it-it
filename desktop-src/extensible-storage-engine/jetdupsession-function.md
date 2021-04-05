---
description: 'Altre informazioni su: funzione JetDupSession'
title: JetDupSession (funzione)
TOCTitle: JetDupSession Function
ms:assetid: fa8fbaca-fe48-401e-9700-1303f4842ad9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294141(v=EXCHG.10)
ms:contentKeyID: 32765755
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupSession
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7aa320c329032f5867f5f762351277cc4567baef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884197"
---
# <a name="jetdupsession-function"></a>JetDupSession (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetdupsession-function"></a>JetDupSession (funzione)

La funzione **JetDupSession** avvia una sessione e Inizializza e restituisce un handle di sessione ESE ([JET_SESID](./jet-sesid.md)). Le sessioni controllano l'accesso al database e vengono utilizzate per controllare l'ambito delle transazioni. La sessione può essere utilizzata per avviare, eseguire il commit o interrompere le transazioni. La sessione viene inoltre utilizzata per il fissaggio, la creazione o l'apertura di un database. La sessione viene utilizzata come contesto per tutte le operazioni DDL e DML. Per aumentare la concorrenza e l'accesso parallelo al database, è possibile iniziare più sessioni.

**Nota** Questa API agirà in tutti i modi come un [JetBeginSession](./jetbeginsession-function.md) chiamato nell'istanza della sessione passata. Questa funzione non è consigliata, [JetBeginSession](./jetbeginsession-function.md) è preferibile.

```cpp
    JET_ERR JET_API JetDupSession(
      __in          JET_SESID sesid,
      __out         JET_SESID* psesid
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare come origine per la duplicazione o l'inizio della sessione.

*psesid*

Un puntatore alla variabile che l'handle di sessione Inizializza per restituire correttamente.

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
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</p>
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
<td><p>L'operazione non è riuscita perché non è stato possibile allocare la memoria.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfSessions</p></td>
<td><p>Il numero di sessioni consentite dal motore per l'avvio del client è limitato. Questo valore può essere modificato utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con la costante <em>JET_paramMaxSessions</em> . Il numero predefinito di sessioni è 16. Per informazioni dettagliate sui <em>JET_paramMaxSessions</em>, vedere <a href="gg294139(v=exchg.10).md">parametri di sistema</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, l'handle di sessione viene inizializzato e può essere utilizzato per le operazioni di database.

In caso di errore, non sono disponibili sessioni o non è stato possibile inizializzare una nuova sessione.

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

[JET_SESID](./jet-sesid.md)  
[JetBeginSession](./jetbeginsession-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
