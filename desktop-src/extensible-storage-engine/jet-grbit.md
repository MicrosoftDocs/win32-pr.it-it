---
description: 'Altre informazioni su: JET_GRBIT'
title: JET_GRBIT
TOCTitle: JET_GRBIT
ms:assetid: b72548cf-3ca2-4ba5-b07a-35eb7e85ed2b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294066(v=EXCHG.10)
ms:contentKeyID: 32765681
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
ms.openlocfilehash: 2b54ed8a95d81c148b68727384dd76fba3d2dc8b1f9d6452c2105bc45f015646
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119362281"
---
# <a name="jet_grbit"></a>JET_GRBIT


_**Si applica a:** Windows | Windows Server_

## <a name="jet_grbit"></a>JET_GRBIT

Il **JET_GRBIT** dati è un gruppo di bit che contengono costanti specifiche per le funzioni e le strutture in cui viene utilizzato.

```cpp
typedef unsigned long JET_GRBIT;
```

### <a name="data-types"></a>Tipi di dati

JET_GRBIT

In generale, le costanti usate come valori per questo tipo di dati riflettono il nome dell'elemento API in cui vengono usate. Ad esempio, tutte le costanti passate [a JetRetrieveColumn](./jetretrievecolumn-function.md) iniziano con "JET_bitRetrieve". Analogamente, tutte le costanti passate a [JetSetColumn](./jetsetcolumn-function.md) iniziano con "JET_bitSet".

Se il valore è zero, il parametro viene ignorato.

### <a name="remarks"></a>Commenti

Per altre informazioni, vedere la funzione o la struttura specifica. Le opzioni vengono in genere passate come set di flag che possono essere combinati.

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

[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)
