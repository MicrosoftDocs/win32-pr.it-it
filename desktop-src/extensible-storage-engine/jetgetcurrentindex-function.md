---
description: 'Altre informazioni su: Funzione JetGetCurrentIndex'
title: Funzione JetGetCurrentIndex
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
ms.openlocfilehash: cb2e1ad0a0f2d4ecab40f582342c0561552a97b3a30ebea785aec7c5fd83fac9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119719151"
---
# <a name="jetgetcurrentindex-function"></a>Funzione JetGetCurrentIndex


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetcurrentindex-function"></a>Funzione JetGetCurrentIndex

La **funzione JetGetCurrentIndex** determina il nome dell'indice corrente di un determinato cursore. Questo nome viene usato anche per selezionare nuovamente l'indice in un secondo momento come indice corrente usando [JetSetCurrentIndex.](./jetsetcurrentindex-function.md) Può essere usato anche per individuare le proprietà dell'indice usando [JetGetTableIndexInfo.](./jetgettableindexinfo-function.md)

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

*tableid*

Cursore da utilizzare per questa chiamata.

*szIndexName*

Buffer di output che riceve il nome dell'indice corrente del cursore.

*cchIndexName*

Dimensione massima in caratteri del buffer di output.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>La stessa sessione non può essere usata per più thread contemporaneamente. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>L'operazione è stata completata correttamente, ma il buffer di output è troppo piccolo per ricevere l'intero nome dell'indice.</p>
<p>Il buffer di output è stato riempito con la maggior parte del nome dell'indice che sarebbe possibile inserire. Se la lunghezza del buffer di output è di almeno un carattere, la stringa in tale buffer di output avrà terminazione Null.</p>
<p><strong>Nota  </strong> Questo errore non verrà restituito se cchIndexName è zero. Per altre informazioni, vedere la sezione Osservazioni.</p></td>
</tr>
</tbody>
</table>


In caso di esito positivo, il nome dell'indice corrente del cursore specificato verrà restituito nel buffer di output. Se JET_wrnBufferTruncated viene restituito , il buffer di output conterrà la quantità di nome dell'indice sufficiente per lo spazio fornito. Se la lunghezza del buffer di output è di almeno un carattere, la stringa restituita in tale buffer avrà terminazione Null. Non verrà apportata alcuna modifica allo stato del database.

In caso di errore, lo stato del buffer di output non sarà definito. Non verrà apportata alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Se non è presente alcun indice corrente per il cursore, verrà restituita una stringa vuota. Questa operazione può verificarsi quando il cursore si trova sull'indice cluster della tabella e non è stato definito alcun indice primario. Questo indice è noto come indice sequenziale della tabella e non ha alcuna definizione. In ogni caso, l'impostazione dell'indice corrente su una stringa vuota tramite [JetSetCurrentIndex](./jetsetcurrentindex-function.md) selezionerà l'indice cluster indipendentemente dalla presenza di una definizione di indice primario.

In questa funzione è presente un bug importante in tutte le versioni. Se il buffer di output è troppo piccolo per ricevere l'intero nome dell'indice e la lunghezza del buffer di output è di almeno un carattere, JET_wrnBufferTruncated non verrà restituito. JET_errSuccess verrà restituito . Per evitare questo problema, il buffer di output deve essere sempre di almeno JET_cbNameMost + 1 (65) caratteri.

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
<td><p>Dichiarato in Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Libreria</strong></p></td>
<td><p>Usare ESENT.lib.</p></td>
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
