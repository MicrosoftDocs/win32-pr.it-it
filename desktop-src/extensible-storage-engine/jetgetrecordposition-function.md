---
description: 'Altre informazioni su: funzione JetGetRecordPosition'
title: Funzione JetGetRecordPosition
TOCTitle: JetGetRecordPosition Function
ms:assetid: 811d9e68-0594-4f70-b854-c3ec966b2705
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269316(v=EXCHG.10)
ms:contentKeyID: 32765606
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d4301b25ca111228b742ce7b35ab9ae28e170526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050112"
---
# <a name="jetgetrecordposition-function"></a>Funzione JetGetRecordPosition


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetrecordposition-function"></a>Funzione JetGetRecordPosition

La funzione **JetGetRecordPosition** restituisce la posizione frazionaria del record corrente nell'indice corrente sotto forma di struttura [JET_RECPOS](./jet-recpos-structure.md) . Questa struttura descrive le posizioni frazionarie in termini di numero approssimativo di voci di indice prima del record corrente e di un numero totale approssimativo di voci nell'indice.

```cpp
    JET_ERR JET_API JetGetRecordPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECPOS* precpos,
      __in          unsigned long cbRecpos
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*TableID*

Cursore da utilizzare per questa chiamata.

*precpos*

Descrizione della frazione da usare per ottenere la posizione del record corrente nell'indice corrente.

*cbRecpos*

Dimensione della memoria allocata in *precpos*.

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
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Questa operazione non può essere completata perché l'istanza di associata alla sessione ha rilevato un errore irreversibile. È necessario che l'accesso a tutti i dati venga revocato per garantire la protezione dell'integrità dei dati.</p>
<p><strong>Windows 2000:</strong>  Questo errore non verrà restituito dal sistema operativo Windows 2000.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Le dimensioni della memoria allocata in <em>precpos</em> non sono sufficienti.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Il cursore non si trova attualmente in un record e non può restituire una posizione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</p>
<p><strong>Windows 2000:</strong>  Questo errore non verrà restituito dal sistema operativo Windows 2000.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, il numero approssimativo di voci di indice che precede il record corrente nell'indice viene restituito in precpos- \> centriesLT. 1 viene restituito in precpos- \> centriesInRange. Il numero approssimativo di voci nell'indice viene restituito in precpos- \> centriesTotal.

In caso di errore, non viene apportata alcuna modifica alla memoria allocata in *precpos*.

#### <a name="remarks"></a>Commenti

Questa operazione restituisce dati variabili quando gli aggiornamenti vengono eseguiti continuamente nella tabella. Le modifiche apportate ai valori non corrisponderanno sempre alle aspettative basate sulla conoscenza degli aggiornamenti, poiché i valori sono approssimazioni basate sulle proprietà fisiche dell'indice. L'isolamento transazionale non si applica alle posizioni da **JetGetRecordPosition** poiché i valori dipendono da proprietà fisiche dell'indice che non sono isolate dalla transazione.

[JET_RECPOS](./jet-recpos-structure.md) non deve essere usato per descrivere un record all'interno di una tabella o per riposizionare un record vicino a un record esistente. Al contrario, è necessario recuperare i segnalibri per un record esistente e quindi utilizzarli per riposizionare lo stesso record.

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

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RECPOS](./jet-recpos-structure.md)  
[JET_SETINFO](./jet-setinfo-structure.md)  
[JetGotoPosition](./jetgotoposition-function.md)  
[JetStopService](./jetstopservice-function.md)
