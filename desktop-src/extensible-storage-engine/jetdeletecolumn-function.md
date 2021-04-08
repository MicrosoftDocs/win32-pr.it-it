---
description: 'Altre informazioni su: funzione JetDeleteColumn'
title: JetDeleteColumn (funzione)
TOCTitle: JetDeleteColumn Function
ms:assetid: b2f4be8c-7ea9-4f66-925b-4e9c14d9d475
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294062(v=EXCHG.10)
ms:contentKeyID: 32765677
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumnA
- JetDeleteColumnW
- JetDeleteColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d7d577447942e36cd49763727473d3f6ddc659b4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "103969529"
---
# <a name="jetdeletecolumn-function"></a>JetDeleteColumn (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetdeletecolumn-function"></a>JetDeleteColumn (funzione)

La funzione **JetDeleteColumn** Elimina una colonna da una tabella di database ESE.

```cpp
JET_ERR JET_API JetDeleteColumn(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName
);
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*TableID*

Tabella da cui eliminare la colonna.

*szColumnName*

Nome della colonna da eliminare.

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
<td><p>JET_errColumnInUse</p></td>
<td><p>La colonna è attualmente in uso. Può essere usato attualmente da un indice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFixedDDL</p></td>
<td><p>È stato effettuato un tentativo di modificare il DDL fisso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFixedInheritedDDL</p></td>
<td><p>La colonna denominata in <em>szColumnName</em> esiste nella tabella del modello e non è possibile modificare il DDL di una tabella modello.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidName</p></td>
<td><p>Questo può essere restituito se è stato specificato un nome non valido per <em>szColumnName</em> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errPermissionDenied</p></td>
<td><p>La tabella non è accessibile in scrittura. Questa operazione può essere restituita se il database è stato aperto in modalità di sola lettura.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTransReadOnly</p></td>
<td><p>La transazione è di sola lettura.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Commenti

La chiamata di **JetDeleteColumn** è identica alla chiamata di [JetDeleteColumn2](./jetdeletecolumn2-function.md) con *grbit* impostato su zero (0).

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
<td><p>Implementato come <strong>JetDeleteColumnW</strong> (Unicode) e <strong>JetDeleteColumnA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetDeleteColumn2](./jetdeletecolumn2-function.md)
