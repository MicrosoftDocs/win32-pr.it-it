---
description: 'Altre informazioni su: struttura JET_INDEXRANGE'
title: Struttura JET_INDEXRANGE
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
ms.openlocfilehash: ecbd8151be8ef278fc1bddc12323f41abd05b09e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315138"
---
# <a name="jet_indexrange-structure"></a>Struttura JET_INDEXRANGE


_**Si applica a:** Windows | Windows Server_

## <a name="jet_indexrange-structure"></a>Struttura JET_INDEXRANGE

La struttura **JET_INDEXRANGE** identifica un intervallo di indice quando viene utilizzato con la funzione [JetIntersectIndexes](./jetintersectindexes-function.md) .

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      JET_GRBIT grbit;
    } JET_INDEXRANGE;
```

### <a name="members"></a>Membri

**cbStruct**

Dimensione, in byte, del **JET_INDEXRANGE**.

**TableID**

Un cursore che in precedenza aveva un intervallo di indici impostato con [JetSetIndexRange](./jetsetindexrange-function.md).

**grbit**

Maschera di maschera costituita esattamente da uno dei seguenti elementi.

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
<td><p>Specifica che l'intervallo di indici deve essere trattato normalmente.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRecordNotInIndex</p></td>
<td><p>Riservato per utilizzi futuri. Non usare.</p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a>Commenti

Ogni **JET_INDEXRANGE** struttura passata a [JetIntersectIndexes](./jetintersectindexes-function.md) rappresenta un intervallo di indici, che verrà intersecato dalla chiamata API. Il cursore specificato in **JET_INDEXRANGE** deve avere già un intervallo di indici valido impostato su di esso, con una chiamata riuscita a [JetSetIndexRange](./jetsetindexrange-function.md).

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
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetIntersectIndexes](./jetintersectindexes-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
