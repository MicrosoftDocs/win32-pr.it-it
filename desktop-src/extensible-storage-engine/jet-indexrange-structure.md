---
description: 'Altre informazioni su: JET_INDEXRANGE struttura'
title: JET_INDEXRANGE struttura
TOCTitle: JET_INDEXRANGE Structure
ms:assetid: 8e437f7d-1e21-4a0b-a5a5-1c78235a4f80
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269335(v=EXCHG.10)
ms:contentKeyID: 32765624
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
ms.openlocfilehash: b5b68e7ebf6df39757ab39947201b945e35a3ece85518a3cb202525033cdd214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118485599"
---
# <a name="jet_indexrange-structure"></a>JET_INDEXRANGE struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_indexrange-structure"></a>JET_INDEXRANGE struttura

La **JET_INDEXRANGE** identifica un intervallo di indici quando viene usato con la [funzione JetIntersectIndexes.](./jetintersectindexes-function.md)

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      JET_GRBIT grbit;
    } JET_INDEXRANGE;
```

### <a name="members"></a>Membri

**cbStruct**

Dimensione, in byte, **dell'oggetto JET_INDEXRANGE**.

**tableid**

Cursore che in precedenza aveva un intervallo di indici impostato [con JetSetIndexRange.](./jetsetindexrange-function.md)

**grbit**

Maschera di bit composta esattamente da uno degli elementi seguenti.

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
<td><p>JET_bitRecordInIndex</p></td>
<td><p>Specifica che l'intervallo di indici deve essere gestito normalmente.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRecordNotInIndex</p></td>
<td><p>Riservato per utilizzi futuri. Non usare.</p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a>Commenti

Ogni **JET_INDEXRANGE** che viene passata a [JetIntersectIndexes](./jetintersectindexes-function.md) rappresenta un intervallo di indici, che verrà intersecato dalla chiamata API. Il cursore specificato **in** JET_INDEXRANGE deve avere già un intervallo di indici valido impostato su di esso, con una chiamata riuscita a [JetSetIndexRange.](./jetsetindexrange-function.md)

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
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetIntersectIndexes](./jetintersectindexes-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
