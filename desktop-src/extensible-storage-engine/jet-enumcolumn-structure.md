---
description: 'Altre informazioni su: JET_ENUMCOLUMN Structure'
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
ms.openlocfilehash: 6ac89a45e37631b554fc7b2dc28266c95cfae3fba54debb427abfd8db621ea3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118766089"
---
# <a name="jet_enumcolumn-structure"></a>Struttura JET_ENUMCOLUMN


_**Si applica a:** Windows | Windows Server_

## <a name="jet_enumcolumn-structure"></a>Struttura JET_ENUMCOLUMN

La **JET_ENUMCOLUMN** enumera i valori di colonna di un record quando viene usata la [funzione JetEnumerateColumns.](./jetenumeratecolumns-function.md) [JetEnumerateColumns](./jetenumeratecolumns-function.md) restituisce una matrice **di** JET_ENUMCOLUMN struttura. La matrice viene restituita in memoria allocata usando il callback compatibile [di rialloca](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito a tale API.

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

**columnid**

ID di colonna enumerato.

**Err**

Codice di stato della colonna derivato dall'enumerazione della colonna.

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
<td><p>L'ID colonna non rientra nei limiti legali di un ID di colonna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>La colonna descritta dall'ID colonna non esiste nella tabella.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnNull</p></td>
<td><p>Tutti i valori per questa colonna sono NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnPresent</p></td>
<td><p>JET_bitEnumeratePresenceOnly è stato specificato e per questa colonna sarebbe stato restituito almeno un valore di colonna diverso da NULL.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnSingleValue</p></td>
<td><p>JET_bitEnumerateCompressOutput è stato specificato ed è stato restituito esattamente un valore di colonna non NULL per questa colonna. Di conseguenza, è stata <strong></strong> restituita la forma JET_ENUMCOLUMN compressa. Vedere <strong>JET_ENUMCOLUMN</strong> per altre informazioni.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnSkipped</p></td>
<td><p>L'ID colonna nello <a href="gg269251(v=exchg.10).md">struct JET_ENUMCOLUMNID</a> corrispondente a <strong>questo</strong> JET_ENUMCOLUMN struct era zero.</p></td>
</tr>
</tbody>
</table>


**cEnumColumnValue**

Matrice di valori di colonna enumerati per la colonna. Il buffer di output viene restituito in memoria allocata usando il callback compatibile di [rialloca](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Questo buffer di output viene usato quando il codice di stato della colonna non è uguale a JET_wrnColumnSingleValue. Per altre informazioni, vedere [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Viene restituito se "err \! = JET_wrnColumnSingleValue".

**rgEnumColumnValue**

Matrice di valori di colonna enumerati per la colonna. Il buffer di output viene restituito in memoria allocata usando il callback compatibile di [rialloca](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Questo buffer di output viene usato quando il codice di stato della colonna non è uguale a JET_wrnColumnSingleValue. Per altre informazioni, vedere [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Viene restituito se "err \! = JET_wrnColumnSingleValue".

**cbData**

Valore della colonna enumerata per la colonna.

Il buffer di output viene restituito in memoria allocata usando il callback compatibile di [rialloca](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Questo buffer di output viene usato solo quando il codice di stato della colonna è JET_wrnColumnSingleValue. Per altre informazioni, vedere [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Viene restituito se "err == JET_wrnColumnSingleValue".

**pvData**

Valore della colonna enumerata per la colonna.

Il buffer di output viene restituito in memoria allocata usando il callback compatibile di [rialloca](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Questo buffer di output viene usato solo quando il codice di stato della colonna è JET_wrnColumnSingleValue. Per altre informazioni, vedere [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Viene restituito se "err == JET_wrnColumnSingleValue".

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
<td><p>Dichiarato in Esent.h.</p></td>
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
