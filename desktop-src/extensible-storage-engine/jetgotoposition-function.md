---
description: 'Altre informazioni su: funzione JetGotoPosition'
title: JetGotoPosition (funzione)
TOCTitle: JetGotoPosition Function
ms:assetid: 77b099f1-4a21-4ddb-b269-83ca74219b4d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269300(v=EXCHG.10)
ms:contentKeyID: 32765592
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aae5148431ad46c5a75bbd804f2c0d777b279561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749719"
---
# <a name="jetgotoposition-function"></a>JetGotoPosition (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetgotoposition-function"></a>JetGotoPosition (funzione)

La funzione **JetGotoPosition** sposta un cursore in una nuova posizione che rappresenta una frazione della strada attraverso l'indice corrente. La frazione è approssimativamente uguale alla seguente:

precpos- \> centriesLT/precpos- \> centriesTotal

Questa operazione viene eseguita in risposta all'input della casella di scorrimento dell'utente che viene ricevuto quando l'utente tenta di visualizzare i dati che iniziano in parte tramite un set di dati.

```cpp
    JET_ERR JET_API JetGotoPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_RECPOS* precpos
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*TableID*

Cursore da utilizzare per questa chiamata.

*precpos*

Descrizione della frazione da utilizzare per posizionare il cursore nell'indice corrente.

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
<td><p>Non è stato possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è stato possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</p>
<p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Il &gt; valore di precpos-cbStruct specificato non è una dimensione valida per la struttura <a href="gg269308(v=exchg.10).md">JET_RECPOS</a> o precpos- &gt; centriesLT è maggiore di precpos- &gt; centriesTotal.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordNotFound</p></td>
<td><p>Questo errore verrà restituito se l'indice è vuoto.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza di associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</p>
<p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p></td>
</tr>
</tbody>
</table>


Se questa funzione ha esito positivo, il cursore viene spostato in un record corrente che rappresenta una frazione della strada attraverso l'indice in cui la frazione è precpos- \> centriesLT divisa per precpos- \> centriesTotal.

Se questa funzione ha esito negativo, la posizione del cursore viene lasciata invariata.

#### <a name="remarks"></a>Commenti

Questa operazione sposta il cursore nella tabella in una posizione nel punto approssimativo seguente: precpos- \> centriesLT diviso per precpos- \> centriesTotal.

Quando si verificano continuamente aggiornamenti sulla tabella, le chiamate successive con lo stesso [JET_RECPOS](./jet-recpos-structure.md) possono spostare il cursore in posizioni diverse nell'indice, sia prima che dopo la posizione precedente. L'isolamento transazionale non si applica al posizionamento tramite [JET_RECPOS](./jet-recpos-structure.md) perché dipende dalle proprietà fisiche dell'indice che non sono isolate dalla transazione.

[JET_RECPOS](./jet-recpos-structure.md) non deve essere usato per descrivere un record all'interno di una tabella o per riposizionare un record vicino a un record esistente. Al contrario, i segnalibri per un record esistente devono essere recuperati dopo un **JetGotoPosition** iniziale e quindi usati per riposizionare lo stesso record.

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
