---
description: 'Altre informazioni su: funzione JetDeleteTable'
title: JetDeleteTable (funzione)
TOCTitle: JetDeleteTable Function
ms:assetid: e8a4131f-a69b-41f3-94c6-a1607fc23c1f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294128(v=EXCHG.10)
ms:contentKeyID: 32765742
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteTable
- JetDeleteTableA
- JetDeleteTableW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c432f8e09ad706b6632e4e5ca49a89a263a84dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319641"
---
# <a name="jetdeletetable-function"></a>JetDeleteTable (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetdeletetable-function"></a>JetDeleteTable (funzione)

La funzione **JetDeleteTable** Elimina una tabella in un database ESE.

```cpp
    JET_ERR JET_API JetDeleteTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*dbid*

Identificatore del database da usare per la chiamata API.

*szTableName*

Nome della tabella da eliminare.

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
<td><p>JET_errTableInUse</p></td>
<td><p>È stato effettuato un tentativo di eliminare una tabella mentre un'altra sessione dispone di un ID di tabella aperto (<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>) con <a href="gg294118(v=exchg.10).md">JetOpenTable</a> o <a href="gg269193(v=exchg.10).md">JetDupCursor</a>.</p></td>
</tr>
<tr class="odd">
<td><p>Tabella JET_errCannotDeletetemporary</p></td>
<td><p>È stato effettuato un tentativo di eliminare una tabella temporanea. Una tabella temporanea viene eliminata automaticamente quando viene chiusa con <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotDeleteTemplateTable</p></td>
<td><p>È stato effettuato un tentativo di eliminare una tabella modello, ovvero una tabella da cui è possibile ereditare DDL.</p></td>
</tr>
</tbody>
</table>


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
<td><p>Implementato come <strong>JetDeleteTableW</strong> (Unicode) e <strong>JetDeleteTableA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_DBID](./jet-dbid.md)  
[JET_SESID](./jet-sesid.md)  
[JetCloseTable](./jetclosetable-function.md)
