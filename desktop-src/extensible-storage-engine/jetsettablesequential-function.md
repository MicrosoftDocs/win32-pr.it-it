---
description: 'Altre informazioni su: funzione JetSetTableSequential'
title: JetSetTableSequential (funzione)
TOCTitle: JetSetTableSequential Function
ms:assetid: 874ddd3c-0d69-4d48-b61a-e9e0457426ef
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269323(v=EXCHG.10)
ms:contentKeyID: 32765613
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b633b348b712e446535054c5a39d2768236b7705
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306212"
---
# <a name="jetsettablesequential-function"></a>JetSetTableSequential (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetsettablesequential-function"></a>JetSetTableSequential (funzione)

La funzione **JetSetTableSequential** notifica al motore di database che l'applicazione esegue l'analisi dell'intero indice corrente contenente un determinato cursore. Di conseguenza, i metodi usati per accedere ai dati dell'indice verranno ottimizzati per rendere questo scenario il più rapido possibile.

**Windows XP:**  **JetSetTableSequential** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetSetTableSequential(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*TableID*

Cursore da utilizzare per questa chiamata.

*grbit*

Gruppo di bit che specifica zero o più delle opzioni seguenti.

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
<td><p>JET_bitPrereadForward</p></td>
<td><p>Questa opzione viene utilizzata per eseguire l'indicizzazione nella direzione avanti.</p>
<p><strong>Windows 7:</strong>  <strong>JET_bitPrereadForward</strong> è stato introdotto in Windows 7.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitPrereadBackward</p></td>
<td><p>Questa opzione viene utilizzata per eseguire l'indicizzazione nella direzione all'indietro.</p>
<p><strong>Windows 7:</strong>  <strong>JET_bitPrereadBackward</strong> è stato introdotto in Windows 7.</p></td>
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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state inattivo in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</p>
<p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza di associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p></td>
</tr>
</tbody>
</table>


Se questa funzione ha esito positivo, l'indice corrente del cursore viene ottimizzato per un'analisi sequenziale dell'intero indice. Non si verificherà alcuna modifica allo stato del database.

Se questa funzione ha esito negativo, non verrà apportata alcuna modifica alla configurazione del cursore. Non si verificherà alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Se l'applicazione deve eseguire un'analisi efficiente di un subset noto di un indice, viene anche eseguita un'ottimizzazione simile ogni volta che viene stabilito un intervallo di indice usando [JetSetIndexRange](./jetsetindexrange-function.md). Questa ottimizzazione è disponibile solo in Windows XP e versioni successive.

Se l'applicazione deve eseguire un'analisi efficiente di un subset sconosciuto di un indice, non è necessario eseguire alcuna azione. Il motore può rilevare automaticamente il comportamento di analisi e recuperare i dati in anticipo. Questo comportamento non è tuttavia troppo aggressivo.

Questa ottimizzazione renderà più efficiente l'analisi dell'indice primario e renderà efficiente l'analisi dei dati delle voci di indice in un indice secondario. Non effettuerà l'analisi di un indice secondario durante il recupero dei dati del record in modo efficiente. Questo perché il motore non esegue un read-ahead sui dati del record.

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008 o Windows Server 2003.</p></td>
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
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)
