---
description: 'Altre informazioni su: funzione JetGetCurrentIndex'
title: JetGetCurrentIndex (funzione)
TOCTitle: JetGetCurrentIndex Function
ms:assetid: 9db3b875-0b95-4027-9742-c36d2d7e64cf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294041(v=EXCHG.10)
ms:contentKeyID: 32765642
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCurrentIndexW
- JetGetCurrentIndex
- JetGetCurrentIndexA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d3337ddaefbea803a137ad8366d2e3df665bacd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315071"
---
# <a name="jetgetcurrentindex-function"></a>JetGetCurrentIndex (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetcurrentindex-function"></a>JetGetCurrentIndex (funzione)

La funzione **JetGetCurrentIndex** determina il nome dell'indice corrente di un determinato cursore. Questo nome viene usato anche per riselezionare in seguito l'indice come indice corrente usando [JetSetCurrentIndex](./jetsetcurrentindex-function.md). Può essere usato anche per individuare le proprietà dell'indice usando [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).

```cpp
    JET_ERR JET_API JetGetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_PSTR szIndexName,
      __in          unsigned long cchIndexName
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*TableID*

Cursore da utilizzare per questa chiamata.

*szIndexName*

Buffer di output che riceve il nome dell'indice corrente del cursore.

*cchIndexName*

Dimensione massima in caratteri del buffer di output.

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
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>L'operazione è stata completata correttamente, ma il buffer di output era troppo piccolo per ricevere l'intero nome di indice.</p>
<p>Il buffer di output è stato riempito con la maggior parte del nome di indice. Se il buffer di output è di almeno un carattere di lunghezza, la stringa in tale buffer di output sarà terminata con null.</p>
<p><strong>Nota  </strong> Questo errore non viene restituito se cchIndexName è zero. Per ulteriori informazioni, vedere la sezione Osservazioni.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, il nome dell'indice corrente del cursore specificato verrà restituito nel buffer di output. Se JET_wrnBufferTruncated viene restituito, il buffer di output conterrà la maggior parte del nome dell'indice che rientrerà nello spazio fornito. Se il buffer di output è di almeno un carattere di lunghezza, la stringa restituita in tale buffer sarà terminata con null. Non si verificherà alcuna modifica allo stato del database.

In caso di errore, lo stato del buffer di output sarà indefinito. Non si verificherà alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Se non è presente alcun indice corrente per il cursore, verrà restituita una stringa vuota. Questo problema può verificarsi quando il cursore si trova nell'indice cluster della tabella e non è stato definito alcun indice primario. Questo indice è noto come indice sequenziale della tabella e non ha alcuna definizione. In ogni caso, l'impostazione dell'indice corrente su una stringa vuota utilizzando [JetSetCurrentIndex](./jetsetcurrentindex-function.md) consente di selezionare l'indice cluster indipendentemente dalla presenza di una definizione di indice primario.

In questa funzione è presente un bug importante presente in tutte le versioni. Se il buffer di output è troppo piccolo per ricevere l'intero nome di indice e il buffer di output è di almeno un carattere di lunghezza, JET_wrnBufferTruncated non verrà restituito. Viene invece restituito JET_errSuccess. Per evitare questo problema, il buffer di output deve contenere sempre almeno JET_cbNameMost + 1 (65) caratteri di lunghezza.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JetGetCurrentIndexW</strong> (Unicode) e <strong>JetGetCurrentIndexA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetSetCurrentIndex](./jetsetcurrentindex-function.md)
