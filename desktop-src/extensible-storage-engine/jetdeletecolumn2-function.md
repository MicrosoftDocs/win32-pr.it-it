---
description: 'Altre informazioni su: funzione JetDeleteColumn2'
title: JetDeleteColumn2 (funzione)
TOCTitle: JetDeleteColumn2 Function
ms:assetid: 840b5acd-8bbf-4524-9741-5d74e3427329
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269320(v=EXCHG.10)
ms:contentKeyID: 32765610
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumn2
- JetDeleteColumn2A
- JetDeleteColumn2W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 35e19eb7ac7b133bb690b268426fec9822efefea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319645"
---
# <a name="jetdeletecolumn2-function"></a>JetDeleteColumn2 (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetdeletecolumn2-function"></a>JetDeleteColumn2 (funzione)

La funzione **JetDeleteColumn2** Elimina una colonna da una tabella di database ESE e consente l'impostazione di un'opzione *grbit* .

**Windows XP: JetDeleteColumn2** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetDeleteColumn2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          const tchar* szColumnName,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*TableID*

Tabella contenente la colonna da eliminare.

*szColumnName*

Nome della colonna da eliminare.

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
<td><p>JET_bitDeleteColumnIgnoreTemplateColumns</p></td>
<td><p>Impostando JET_bitDeleteColumIgnoreTemplateColumns si farà in modo che l'API tenti di eliminare solo le colonne nella tabella derivata. Se una colonna con tale nome esiste nella tabella di base, verrà ignorata.</p></td>
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

La chiamata di [JetDeleteColumn](./jetdeletecolumn-function.md) è identica alla chiamata di **JetDeleteColumn2** con *grbit* impostato su zero (0).

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JetDeleteColumn2W</strong> (Unicode) e <strong>JetDeleteColumn2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetDeleteColumn](./jetdeletecolumn-function.md)
