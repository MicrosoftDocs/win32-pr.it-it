---
description: 'Altre informazioni su: funzione JetPrepareUpdate'
title: JetPrepareUpdate (funzione)
TOCTitle: JetPrepareUpdate Function
ms:assetid: 90cbaa83-47f2-4a65-b561-3bdecb7fd95a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269339(v=EXCHG.10)
ms:contentKeyID: 32765628
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrepareUpdate
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16362463194d945d7b451f784bc0942bda2d03e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319176"
---
# <a name="jetprepareupdate-function"></a>JetPrepareUpdate (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetprepareupdate-function"></a>JetPrepareUpdate (funzione)

La funzione **JetPrepareUpdate** è la prima operazione di esecuzione di un aggiornamento, allo scopo di inserire un nuovo record o di sostituire un record esistente con nuovi valori. Gli aggiornamenti vengono eseguiti chiamando **JetPrepareUpdate**, quindi chiamando [JetSetColumn](./jetsetcolumn-function.md) o [JetSetColumns](./jetsetcolumns-function.md) zero o più volte e infine chiamando [JetUpdate](./jetupdate-function.md) per completare l'operazione. **JetPrepareUpdate** e [JetUpdate](./jetupdate-function.md) impostano i limiti per un'operazione di aggiornamento e sono importanti per avere solo lo stato di aggiornamento finale di un record immesso negli indici. Questa operazione è più efficiente, ma anche obbligatoria nei casi in cui i dati devono corrispondere a uno stato valido tramite più di un'operazione set Column.

Sono disponibili diverse opzioni per l'inserimento o la sostituzione dei record, che sono descritte in dettaglio di seguito.

```cpp
    JET_ERR JET_API JetPrepareUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long prep
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*TableID*

Cursore da utilizzare per questa chiamata.

*Prep*

Opzioni che possono essere utilizzate per preparare un aggiornamento, incluse le seguenti.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valore</p></th>
<th><p>Significato</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_prepCancel</p></td>
<td><p>Questo flag fa in modo che <strong>JetPrepareUpdate</strong> annulli l'aggiornamento per questo cursore.</p></td>
</tr>
<tr class="even">
<td><p>JET_prepInsert</p></td>
<td><p>Questo flag determina la preparazione del cursore per l'inserimento di un nuovo record. Tutti i dati vengono inizializzati sullo stato predefinito per il record. Se la tabella include una colonna con incremento automatico, a questo record viene assegnato un nuovo valore indipendentemente dal fatto che l'aggiornamento abbia esito positivo o negativo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_prepInsertCopy</p></td>
<td><p>Questo flag determina la preparazione del cursore per l'inserimento di una copia del record esistente. Se viene utilizzata questa opzione, deve essere presente un record corrente. Lo stato iniziale del nuovo record viene copiato dal record corrente. I valori Long archiviati in modalità non registrata vengono copiati virtualmente.</p></td>
</tr>
<tr class="even">
<td><p>JET_prepInsertCopyDeleteOriginal</p></td>
<td><p>Questo flag determina la preparazione del cursore per un inserimento dello stesso record e per l'eliminazione o il record originale. Viene utilizzato nei casi in cui la chiave primaria è stata modificata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_prepReplace</p></td>
<td><p>Questo flag determina la preparazione del cursore per la sostituzione del record corrente. Se la tabella contiene una colonna versione, la colonna Version viene impostata sul valore successivo nella sequenza. Se l'aggiornamento non viene completato, il valore della versione nel record non sarà interessato. Viene assunto un blocco di aggiornamento sul record per impedire ad altre sessioni di aggiornare questo record prima del completamento della sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_prepReplaceNoLock</p></td>
<td><p>Questo flag è simile a JET_prepReplace, ma non viene effettuato alcun blocco per impedire ad altre sessioni di aggiornare questo record. Questa sessione può invece ricevere JET_errWriteConflict quando chiama <a href="gg269288(v=exchg.10).md">JetUpdate</a> per completare l'aggiornamento.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errAlreadyPrepared</p></td>
<td><p><strong>JetPrepareUpdate</strong> è stato chiamato con un flag valido per la preparazione ma non JET_prepCancel e il cursore si trovava già nello stato preparato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Il flag di preparazione specificato non è un flag valido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInTransaction</p></td>
<td><p><strong>JetPrepareUpdate</strong> è stato chiamato per sostituire un record con colonne SLV. Colonne SLV. Si noti che le colonne SLV sono una funzionalità non destinata all'utilizzo generale. Questa funzionalità viene utilizzata per supportare l'infrastruttura di Microsoft Exchange e non deve essere utilizzata nell'applicazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRollbackError</p></td>
<td><p><strong>JetPrepareUpdate</strong> è stato chiamato con JET_prepCancel ma non è stato possibile eseguire il rollback di tutte le modifiche apportate alle colonne di tipo JET_coltypLongText e/o alle colonne di tipo JET_coltypLongBinary.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare questo flag con la stessa sessione da più di un thread nello stesso momento. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errUpdateNotPrepared</p></td>
<td><p><strong>JetPrepareUpdate</strong> è stato chiamato con JET_prepCancel ma il cursore non si trovava nello stato preparato.</p></td>
</tr>
</tbody>
</table>


In caso di esito positivo, il cursore viene impostato sullo stato preparato per lo scopo dell'aggiornamento desiderato o, nel caso di JET_prepCancel, il cursore viene ripristinato allo stato non preparato e tutte le modifiche vengono ignorate.

In caso di errore, lo stato del cursore viene lasciato invariato. Se l'errore è stato JET_errRollbackError, lo stato del cursore viene modificato nello stato non preparato, ma non tutte le modifiche sono state ripristinate.

#### <a name="remarks"></a>Commenti

L'inserimento di una copia di un record è un'ottimizzazione importante quando i record condividono dati di tipo JET_coltypLongText e/o JET_coltypLongBinary. Questi dati vengono archiviati in modalità non registrata quando è grande ed è possibile che più record condividano la stessa rappresentazione fisica dei dati. In questo caso, i dati possono essere aggiornati da uno dei due record, ma in questo modo i dati verranno incrementati in modo tale che ogni record disponga di una propria copia. Non è possibile modificare i dati in un record mediante una modifica da un altro record. Non è inoltre possibile bloccare un aggiornamento di un record tramite un aggiornamento di un altro record. Si tratta di una funzionalità centrale di ESE ed è nota come blocco a livello di record.

Le operazioni [JetUpdate](./jetupdate-function.md) che non riescono lasciano il cursore nello stato preparato per l'aggiornamento. Questo consente la correzione ad alcuni errori, ad esempio un valore di colonna errato, senza che sia necessario ricreare lo stato di aggiornamento. Ciò significa che in tutti i casi in cui un cursore abbandona un aggiornamento, deve chiamare in modo esplicito **JetPrepareUpdate** con JET_prepCancel.

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
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)  
[JetUpdate](./jetupdate-function.md)
