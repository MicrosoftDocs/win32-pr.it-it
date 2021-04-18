---
description: 'Altre informazioni su: struttura JET_ENUMCOLUMNVALUE'
title: Struttura JET_ENUMCOLUMNVALUE
TOCTitle: JET_ENUMCOLUMNVALUE Structure
ms:assetid: a9882d7b-0c53-4a5d-bc98-0979e6e68c88
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294052(v=EXCHG.10)
ms:contentKeyID: 32765652
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bc95c6b8403a64432451ea29dbb66868fad25264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316487"
---
# <a name="jet_enumcolumnvalue-structure"></a>Struttura JET_ENUMCOLUMNVALUE


_**Si applica a:** Windows | Windows Server_

## <a name="jet_enumcolumnvalue-structure"></a>Struttura JET_ENUMCOLUMNVALUE

La struttura **JET_ENUMCOLUMNVALUE** enumera i valori di colonna di un record utilizzando la funzione [JetEnumerateColumns](./jetenumeratecolumns-function.md) . [JetEnumerateColumns](./jetenumeratecolumns-function.md) restituisce una matrice di strutture di **JET_ENUMCOLUMNVALUE** . La matrice viene restituita nella memoria allocata utilizzando il callback compatibile con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito a tale funzione.

```cpp
    typedef struct {
      unsigned long itagSequence;
      JET_ERR err;
      unsigned long cbData;
      void* pvData;
    } JET_ENUMCOLUMNVALUE;
```

### <a name="members"></a>Membri

**itagSequence**

Valore della colonna (in base a un indice in base 1) enumerato.

**Err**

Codice di stato della colonna risultante dall'enumerazione del valore della colonna.

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
<td><p>JET_wrnColumnNull</p></td>
<td><p>Il valore della colonna richiesto è NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnSkipped</p></td>
<td><p>Il <em>itagSequence</em> specificato nell'elemento della matrice <em>rgtagSequence</em> nello struct <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> corrispondente a questo struct di <strong>JET_ENUMCOLUMNVALUE</strong> è zero.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnTruncated</p></td>
<td><p>Il valore della colonna richiesta è stato troncato alla dimensione specificata prima di essere restituito.</p>
<p>Questo troncamento si verifica solo per il testo lungo e per le colonne binarie lunghe che contengono grandi quantità di dati.</p></td>
</tr>
</tbody>
</table>


**cbData**

Valore di colonna enumerato per la colonna.

Il buffer di output viene restituito nella memoria allocata mediante il callback compatibile con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

**pvData**

Valore di colonna enumerato per la colonna.

Il buffer di output viene restituito nella memoria allocata mediante il callback compatibile con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

### <a name="requirements"></a>Requisiti

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
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNVALUE]()  
[JET_ERR](./jet-err.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
