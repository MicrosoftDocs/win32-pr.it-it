---
description: 'Altre informazioni su: funzione JetEndSession'
title: JetEndSession (funzione)
TOCTitle: JetEndSession Function
ms:assetid: a9a8f98a-258e-4fbb-bed0-657581984a07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294054(v=EXCHG.10)
ms:contentKeyID: 32765660
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndSession
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46bea6f5db745252a5e0ac6e8e03550dfead1b43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346666"
---
# <a name="jetendsession-function"></a>JetEndSession (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetendsession-function"></a>JetEndSession (funzione)

La funzione **JetEndSession** termina la sessione e pulisce e dealloca le risorse associate alla sessione specificata.

```cpp
    JET_ERR JET_API JetEndSession(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da terminare. Le risorse associate vengono rilasciate al termine della sessione.

*grbit*

Riservato. Questo parametro può contenere il flag di JET_bitForceSessionClosed, ma questo flag è riservato e l'impostazione non ha alcun effetto.

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
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti contiene un valore imprevisto o la combinazione di diversi valori di parametro ha restituito un risultato imprevisto.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>La sessione non è una sessione JET valida.</p></td>
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
<td><p>JET_errSessionInUse</p></td>
<td><p>Ciò significa che la sessione è stata usata in un altro thread o che la sessione non è stata impostata o reimpostata correttamente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</p>
<p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfBuffers</p></td>
<td><p>Errore di sistema che indica che non sono presenti altri buffer.</p></td>
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


In seguito all'esito positivo, l'handle di sessione viene chiuso e non è disponibile e tutte le risorse correlate a questa sessione vengono pulite.

In caso di errore, è possibile che si verifichino alcuni errori aggiuntivi come parte della chiusura della tabella di ordinamento, della chiusura del cursore e del rollback della transazione. Questi errori sono piuttosto improbabili ed estremamente improbabili se le sessioni non vengono usate completamente quando viene chiamato **JetEndSession** . Questi errori verranno restituiti se non è stato possibile pulire correttamente una parte della sessione.

#### <a name="remarks"></a>Commenti

Questa API esegue il rollback di tutte le transazioni aperte (non sottoposte a commit nel livello 0). Verranno puliti anche tutti i cursori associati alla sessione e le tabelle di ordinamento create o aperte.

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

[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginSession](./jetbeginsession-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)
