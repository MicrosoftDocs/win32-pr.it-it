---
description: 'Altre informazioni su: funzione JetDelete'
title: Funzione JetDelete
TOCTitle: JetDelete Function
ms:assetid: 807de5ba-2f4b-4779-ab29-a1f094beecc1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269315(v=EXCHG.10)
ms:contentKeyID: 32765605
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDelete
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f3422bc623bbd4f0cc99365df51bb797100811c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315622"
---
# <a name="jetdelete-function"></a>Funzione JetDelete


_**Si applica a:** Windows | Windows Server_

## <a name="jetdelete-function"></a>Funzione JetDelete

La funzione **JetDelete** Elimina il record corrente in una tabella di database.

```cpp
    JET_ERR JET_API JetDelete(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione del database che verrà usato per la chiamata API.

*TableID*

Cursore su una tabella di database. La riga corrente verrà eliminata.

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
<td><p>JET_errCallbackFailed</p></td>
<td><p>La funzione di callback ha avuto esito negativo in qualche modo. Le violazioni di accesso nelle funzioni di callback, ad esempio, vengono rilevate e convertite in JET_errCallbackFailed. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIllegalOperation</p></td>
<td><p>Il cursore specificato da <em>TableID</em> non supporta l'eliminazione. Vedere la sezione relativa alle osservazioni.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Il cursore specificato da <em>TableID</em> non si trova in un record.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPermissionDenied</p></td>
<td><p>Il motore di database non dispone di autorizzazioni sufficienti per eliminare il record. Questo problema può verificarsi se il file di database è stato aperto con accesso in sola lettura.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRollbackError</p></td>
<td><p>Un buffer di aggiornamento (vedere <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>) esiste, ma non è possibile eseguire il rollback di tutte le modifiche apportate alle colonne di tipo JET_coltypLongText e/o colonne di tipo JET_coltypLongBinary.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è consentito usare la stessa sessione da più di un thread nello stesso momento. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTransReadOnly</p></td>
<td><p>La transazione è di sola lettura e non supporta le eliminazioni.</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemory</p></td>
<td><p>Operazione non riuscita perché la memoria disponibile non è sufficiente per mantenere le informazioni transazionali sull'aggiornamento.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict</p></td>
<td><p>Un'altra sessione ha bloccato in precedenza il record per l'aggiornamento. Il tentativo di aggiornamento da questa sessione avrà esito negativo.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, la valuta viene lasciata immediatamente prima del record successivo. Se il record eliminato era l'ultimo nella tabella, la valuta viene lasciata alla fine della tabella, ovvero dopo il nuovo record. Se il record eliminato è l'unico record della tabella, la valuta viene impostata all'inizio.

Gli indici appropriati vengono aggiornati automaticamente.

Se un aggiornamento viene preparato (usando [JetPrepareUpdate](./jetprepareupdate-function.md)), verrà annullato. Il buffer di aggiornamento verrà reimpostato.

In caso di errore, la valuta rimane invariata. Se un aggiornamento viene preparato (vedere [JetPrepareUpdate](./jetprepareupdate-function.md)), il buffer di aggiornamento potrebbe essere reimpostato.

#### <a name="remarks"></a>Commenti

Non tutte le tabelle supportano l'eliminazione di righe. Una tabella temporanea in genere non supporta l'eliminazione di righe. L'eliminazione di record può essere abilitata nelle tabelle temporanee per diversi motivi, alcune delle quali sono:

  - JET_bitTTUpdatable specificato durante la creazione.

  - Le tabelle temporanee di grandi dimensioni possono supportare l'eliminazione se sono state create con JET_bitTTScrollable o JET_bitTTIndexed. La soglia in corrispondenza della quale una tabella temporanea diventa "large" è attualmente 64 kilobyte, ma potrebbe essere modificata nelle versioni future.

Windows XP e versioni successive. Le funzioni di callback possono essere richiamate da **JetDelete**, inclusi JET_cbtypBeforeDelete e JET_cbtypAfterDelete.

È importante comprendere l'effetto dell'esecuzione di un numero elevato di operazioni di aggiornamento all'interno di una singola transazione. Ogni aggiornamento del database deve essere rilevato dal motore di database nell'archivio delle versioni. L'archivio versione include un record live di tutte le diverse versioni di ogni voce di record o di indice nel database che possono essere visualizzate da tutte le transazioni attive. Queste versioni vengono utilizzate per supportare il controllo della concorrenza multiversione utilizzato dal motore di database per supportare le transazioni mediante l'isolamento dello snapshot. Una volta che il motore di database ha esaurito le risorse usate per archiviare queste versioni, non può più accettare ulteriori modifiche fino a quando alcune transazioni non sono state terminate per consentire il ripristino di queste risorse. Quando il motore è in questo stato, tutti gli aggiornamenti avranno esito negativo con JET_errVersionStoreOutOfMemory. Le risorse disponibili per il motore di database per archiviare queste versioni possono essere controllate utilizzando [JetSetSystemParameter](./jetsetsystemparameter-function.md) con *JET_paramMaxVerPages* e *JET_paramGlobalMinVerPages*.

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
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
