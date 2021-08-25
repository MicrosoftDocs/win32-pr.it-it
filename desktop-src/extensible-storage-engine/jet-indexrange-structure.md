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
ms.openlocfilehash: 48e9da5822f69d4460a1699252112899a990188d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470877"
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


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitRecordInIndex</p> | <p>Specifica che l'intervallo di indici deve essere gestito normalmente.</p> | 
| <p>JET_bitRecordNotInIndex</p> | <p>Riservato per utilizzi futuri. Non usare.</p> | 



### <a name="remarks"></a>Commenti

Ogni **JET_INDEXRANGE** che viene passata a [JetIntersectIndexes](./jetintersectindexes-function.md) rappresenta un intervallo di indici, che verrà intersecato dalla chiamata API. Il cursore specificato **in** JET_INDEXRANGE deve avere già un intervallo di indici valido impostato su di esso, con una chiamata riuscita a [JetSetIndexRange.](./jetsetindexrange-function.md)

### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetIntersectIndexes](./jetintersectindexes-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
