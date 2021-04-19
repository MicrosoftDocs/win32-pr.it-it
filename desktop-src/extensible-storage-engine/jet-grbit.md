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
ms.openlocfilehash: b050aaa844ea814c0c24a62ccfb5ab332c611107
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323779"
---
# <a name="jet_grbit"></a>JET_GRBIT


_**Si applica a:** Windows | Windows Server_

## <a name="jet_grbit"></a>JET_GRBIT

Il tipo di dati **JET_GRBIT** è costituito da un gruppo di bit che contengono costanti specifiche per le funzioni e le strutture in cui vengono utilizzate.

```cpp
typedef unsigned long JET_GRBIT;
```

### <a name="data-types"></a>Tipi di dati

JET_GRBIT

In generale, le costanti utilizzate come valori per questo tipo di dati riflettono il nome dell'elemento API in cui vengono utilizzate. Ad esempio, tutte le costanti passate a [JetRetrieveColumn](./jetretrievecolumn-function.md) iniziano con "JET_bitRetrieve". Analogamente, tutte le costanti passate a [JetSetColumn](./jetsetcolumn-function.md) iniziano con "JET_bitSet".

Se il valore è zero, il parametro viene ignorato.

### <a name="remarks"></a>Commenti

Per ulteriori informazioni, vedere la funzione o la struttura specifica. Le opzioni vengono in genere passate come un set di flag che possono essere combinati.

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

[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)
