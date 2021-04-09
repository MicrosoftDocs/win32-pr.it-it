---
description: 'Altre informazioni su: struttura JET_ENUMCOLUMN'
title: Struttura JET_ENUMCOLUMN
TOCTitle: JET_ENUMCOLUMN Structure
ms:assetid: f8f512fd-5fcf-47ed-a5db-2fb3bd76c2d7
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294138(v=EXCHG.10)
ms:contentKeyID: 32765752
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
ms.openlocfilehash: ca204fef4e67e6883584511b1ac424149a137b79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128223"
---
# <a name="jet_enumcolumn-structure"></a>Struttura JET_ENUMCOLUMN


_**Si applica a:** Windows | Windows Server_

## <a name="jet_enumcolumn-structure"></a>Struttura JET_ENUMCOLUMN

La struttura **JET_ENUMCOLUMN** enumera i valori di colonna di un record quando viene utilizzata la funzione [JetEnumerateColumns](./jetenumeratecolumns-function.md) . [JetEnumerateColumns](./jetenumeratecolumns-function.md) restituisce una matrice di strutture di **JET_ENUMCOLUMN** . La matrice viene restituita nella memoria allocata usando il callback compatibile con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito a tale API.

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      JET_ERR err;
      union {
        struct {
          unsigned long cEnumColumnValue;
          JET_ENUMCOLUMNVALUE rgEnumColumnValue;
        };
        struct {
          unsigned long cbData;
          void* pvData;
        };
      };
    } JET_ENUMCOLUMN;
```

### <a name="members"></a>Membri

**ColumnID**

ID di colonna enumerato.

**Err**

Codice di stato della colonna risultante dall'enumerazione della colonna.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Codici errore</p></th>
<th><p>Significato</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errBadColumnId</p></td>
<td><p>L'ID di colonna non rientra nei limiti validi di un ID di colonna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>La colonna descritta dall'ID di colonna non esiste nella tabella.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnNull</p></td>
<td><p>Tutti i valori per questa colonna sono NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnPresent</p></td>
<td><p>È stato specificato JET_bitEnumeratePresenceOnly e per questa colonna è stato restituito almeno un valore di colonna non NULL.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnSingleValue</p></td>
<td><p>JET_bitEnumerateCompressOutput è stato specificato ed è stato restituito esattamente un valore di colonna non NULL per questa colonna. Di conseguenza, viene restituito il formato compresso di <strong>JET_ENUMCOLUMN</strong> . Per ulteriori informazioni, vedere <strong>JET_ENUMCOLUMN</strong> .</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnSkipped</p></td>
<td><p>L'ID di colonna nello struct <a href="gg269251(v=exchg.10).md">JET_ENUMCOLUMNID</a> corrispondente a questo struct di <strong>JET_ENUMCOLUMN</strong> è zero.</p></td>
</tr>
</tbody>
</table>


**cEnumColumnValue**

Matrice di valori di colonna enumerata per la colonna. Il buffer di output viene restituito nella memoria allocata mediante il callback compatibile con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Questo buffer di output viene utilizzato quando il codice di stato della colonna non è uguale a JET_wrnColumnSingleValue. Per ulteriori informazioni, vedere [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Viene restituito se "ERR \! = JET_wrnColumnSingleValue".

**rgEnumColumnValue**

Matrice di valori di colonna enumerata per la colonna. Il buffer di output viene restituito nella memoria allocata mediante il callback compatibile con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Questo buffer di output viene utilizzato quando il codice di stato della colonna non è uguale a JET_wrnColumnSingleValue. Per ulteriori informazioni, vedere [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Viene restituito se "ERR \! = JET_wrnColumnSingleValue".

**cbData**

Valore di colonna enumerato per la colonna.

Il buffer di output viene restituito nella memoria allocata mediante il callback compatibile con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Questo buffer di output viene utilizzato solo quando il codice di stato della colonna viene JET_wrnColumnSingleValue. Per ulteriori informazioni, vedere [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Viene restituito se "Err = = JET_wrnColumnSingleValue".

**pvData**

Valore di colonna enumerato per la colonna.

Il buffer di output viene restituito nella memoria allocata mediante il callback compatibile con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Questo buffer di output viene utilizzato solo quando il codice di stato della colonna viene JET_wrnColumnSingleValue. Per ulteriori informazioni, vedere [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Viene restituito se "Err = = JET_wrnColumnSingleValue".

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

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_ENUMCOLUMNID](./jet-enumcolumnid-structure.md)  
[JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
