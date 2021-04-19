---
description: 'Altre informazioni su: funzione JetDeleteIndex'
title: JetDeleteIndex (funzione)
TOCTitle: JetDeleteIndex Function
ms:assetid: c540503b-d5a6-47f2-9113-9650891c4b6d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294081(v=EXCHG.10)
ms:contentKeyID: 32765696
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteIndexW
- JetDeleteIndexA
- JetDeleteIndex
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 52a29e619d6643df4984bd7f296dcef4ef0a5ccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319179"
---
# <a name="jetdeleteindex-function"></a>JetDeleteIndex (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetdeleteindex-function"></a>JetDeleteIndex (funzione)

La funzione **JetDeleteIndex** Elimina un indice da una tabella.

```cpp
    JET_ERR JET_API JetDeleteIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*TableID*

Tabella contenente la colonna da eliminare.

*szIndexName*

Nome dell'indice da eliminare.

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
<td><p>JET_errFixedDDL</p></td>
<td><p>È stato effettuato un tentativo di eliminare un indice da una tabella fissa (ad esempio, uno creato con JET_bitTableCreateFixedDDL).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFixedInheritedDDL</p></td>
<td><p>È stato effettuato un tentativo di eliminare un indice da una tabella del modello. Una tabella modello ha un linguaggio DDL fisso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexNotFound</p></td>
<td><p>L'indice denominato in <em>szIndexName</em> non è stato trovato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPermissionDenied</p></td>
<td><p>Impossibile aggiornare la tabella perché è stata aperta in sola lettura.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Più thread hanno tentato di usare la stessa sessione di database.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTransReadOnly</p></td>
<td><p>La transazione è stata aperta come transazione di sola lettura.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Commenti

In caso di esito positivo, l'indice viene eliminato e pertanto non può essere utilizzato successivamente. Non deve essere presente alcuna transazione attiva utilizzando l'indice.

In seguito all'esito positivo, la valuta viene impostata prima del primo record.

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
<td><p>Implementato come <strong>JetDeleteIndexW</strong> (Unicode) e <strong>JetDeleteIndexA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)
