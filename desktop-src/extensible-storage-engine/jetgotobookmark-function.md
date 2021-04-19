---
description: 'Altre informazioni su: funzione JetGotoBookmark'
title: JetGotoBookmark (funzione)
TOCTitle: JetGotoBookmark Function
ms:assetid: a9a0aa43-834a-4eec-b47f-8e74d35aa972
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294053(v=EXCHG.10)
ms:contentKeyID: 32765656
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 89dde261648b396bcfc9532911c0d4acd3c88828
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318090"
---
# <a name="jetgotobookmark-function"></a>JetGotoBookmark (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetgotobookmark-function"></a>JetGotoBookmark (funzione)

La funzione **JetGotoBookmark** posiziona un cursore in una voce di indice per il record associato al segnalibro specificato. Il segnalibro può essere utilizzato con qualsiasi indice definito in una tabella. Il segnalibro per un record può essere recuperato usando [JetGetBookmark](./jetgetbookmark-function.md).

```cpp
    JET_ERR JET_API JetGotoBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvBookmark,
      __in          unsigned long cbBookmark
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*TableID*

Cursore da utilizzare per questa chiamata.

*pvBookmark*

Buffer che contiene il segnalibro da utilizzare per posizionare il cursore.

*cbBookmark*

Dimensioni del segnalibro nel buffer.

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
<p><strong>Windows XP:</strong>   Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBookmark</p></td>
<td><p>Il segnalibro fornito non è valido. Questa situazione potrebbe essersi verificata perché le dimensioni del segnalibro sono pari a zero oppure il puntatore del buffer del segnalibro è <strong>null</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Il cursore si trova in un indice secondario e non è stata trovata alcuna voce di indice per il record associato al segnalibro.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordDeleted</p></td>
<td><p>Impossibile trovare il record associato al segnalibro.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza di associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</p>
<p><strong>Windows XP:</strong>   Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p></td>
</tr>
</tbody>
</table>


Se questa funzione ha esito positivo, il cursore verrà posizionato in corrispondenza di una voce di indice per il record associato al segnalibro specificato. Se un record è stato preparato per l'aggiornamento, l'aggiornamento verrà annullato. Se è attivo un intervallo di indici, l'intervallo di indici verrà annullato. Se è stata creata una chiave di ricerca per il cursore, tale chiave di ricerca verrà eliminata. Non si verificherà alcuna modifica allo stato del database.

Se questa funzione ha esito negativo, la posizione del cursore rimarrà invariata. Se un record è stato preparato per l'aggiornamento, l'aggiornamento verrà annullato. Se è attivo un intervallo di indici, l'intervallo di indici verrà annullato. Se è stata creata una chiave di ricerca per il cursore, tale chiave di ricerca verrà eliminata. Non si verificherà alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Esistono due modi per utilizzare un segnalibro per posizionare un cursore su un indice. Il primo consiste nell'usare il segnalibro per posizionare direttamente il record. Questo errore si verifica quando l'indice corrente del cursore è l'indice primario. Questa tecnica funziona perché un segnalibro ESENT è uguale alla chiave primaria del record associato.

Il secondo modo per usare un segnalibro è posizionarlo in una voce in un indice secondario che corrisponde al record associato a tale segnalibro. Durante questo processo, il motore cerca il record effettivo utilizzando il segnalibro nell'indice primario. USA quindi i dati del record e la definizione dell'indice secondario per calcolare una chiave nell'indice secondario che punta al record. Quindi posiziona il cursore sulla voce di indice per tale chiave. Se il cursore si trova attualmente in un indice secondario su una o più colonne chiave multivalore, il cursore verrà posizionato sulla voce di indice corrispondente al primo multivalore di ognuna di queste colonne chiave.

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
[JetGetBookmark](./jetgetbookmark-function.md)
