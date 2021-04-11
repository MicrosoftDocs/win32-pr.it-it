---
description: 'Altre informazioni su: funzione JetGetLock'
title: JetGetLock (funzione)
TOCTitle: JetGetLock Function
ms:assetid: cebf0789-3d31-4ae8-9b23-dcf5e34e98fc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294094(v=EXCHG.10)
ms:contentKeyID: 32765709
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLock
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5757616214336de25ce30ca49755ac229b10afbe
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104132434"
---
# <a name="jetgetlock-function"></a>JetGetLock (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetlock-function"></a>JetGetLock (funzione)

La funzione **JetGetLock** fornisce un mezzo per riservare in modo esplicito la possibilità di aggiornare una riga, un blocco di scrittura o di impedire in modo esplicito l'aggiornamento di una riga da qualsiasi altra sessione, ovvero il blocco di lettura. In genere, i blocchi di scrittura di riga vengono acquisiti in modo implicito in seguito all'aggiornamento delle righe. I blocchi di lettura non sono in genere necessari a causa del controllo delle versioni dei record. Tuttavia, in alcuni casi è possibile che una transazione desideri bloccare in modo esplicito una riga per applicare la serializzazione o per assicurarsi che un'operazione successiva abbia esito positivo in virtù del fatto che i blocchi necessari sono già stati eseguiti.

```cpp
JET_ERR JET_API JetGetLock(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione che verrà utilizzata per questa chiamata.

*TableID*

Cursore che verrà utilizzato per la chiamata.

*grbit*

Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più degli elementi seguenti:

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
<td><p>JET_bitReadLock</p></td>
<td><p>Questo flag causa l'acquisizione di un blocco di lettura nel record corrente. I blocchi di lettura non sono compatibili con i blocchi di scrittura già conservati da altre sessioni, ma sono compatibili con i blocchi di lettura mantenuti da altre sessioni.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitWriteLock</p></td>
<td><p>Questo flag determina l'acquisizione di un blocco di scrittura nel record corrente. I blocchi di scrittura non sono compatibili con i blocchi Write o Read utilizzati da altre sessioni, ma sono compatibili con i blocchi di lettura contenuti nella stessa sessione.</p></td>
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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Il <em>grbit</em> specificato non è JET_bitReadLock o JET_bitWriteLock. Deve essere uno di questi due flag.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Per poter acquisire un blocco, il cursore deve trovarsi in un record. I blocchi sono sempre presenti nei record.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInTransaction</p></td>
<td><p>I blocchi possono essere acquisiti solo da sessioni in una transazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPermissionDenied</p></td>
<td><p>Il cursore non può essere di sola lettura e acquisire un blocco di scrittura.</p></td>
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
<td><p>JET_errTransReadOnly</p></td>
<td><p>La sessione deve disporre delle autorizzazioni di scrittura per acquisire il blocco di scrittura.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict</p></td>
<td><p>Errore restituito quando viene richiesto un blocco in conflitto.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, la sessione ha acquisito il blocco richiesto.

In caso di errore, la sessione non ha acquisito il blocco richiesto.

#### <a name="remarks"></a>Commenti

Non è possibile acquisire blocchi di scrittura con sessioni o cursori che dispongono di autorizzazioni di sola lettura, anche se la sessione e il cursore non eseguono un'operazione di aggiornamento. Sia la sessione che il cursore devono disporre dei privilegi di scrittura per acquisire un blocco di scrittura.

I blocchi di lettura e scrittura sono un metodo di blocco pessimistico. Il blocco pessimistico prevede più sessioni simultanee per il conflitto e acquisisce i blocchi in anticipo per assicurarsi che le operazioni abbiano esito positivo.

La maggior parte delle operazioni sarà serializzabile in base ai blocchi acquisiti in modo implicito. Tuttavia, alcune operazioni non lo sono. Per illustrare questo problema, prendere in considerazione le due transazioni,

T1: R (A), U (B)

T2: R (B), U (A)

Il controllo delle versioni A livello di record garantisce che ogni transazione eseguita contemporaneamente visualizzerà i valori originali per A e B. Non esiste un ordine seriale di esecuzione che può produrre gli stessi risultati per A e B, nel caso in cui i risultati dipendano dai dati letti. Per rendere serializzabile questa transazione, l'applicazione deve acquisire un blocco di lettura esplicito su A e B in ogni transazione quando viene letto il valore.

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
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetUpdate](./jetupdate-function.md)
