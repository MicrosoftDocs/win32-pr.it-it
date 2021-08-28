---
description: 'Altre informazioni su: JET_INDEXID struttura'
title: JET_INDEXID struttura
TOCTitle: JET_INDEXID Structure
ms:assetid: 8b1d90f0-bc93-4b30-90d1-b9e93ad26654
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269327(v=EXCHG.10)
ms:contentKeyID: 32765617
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
ms.openlocfilehash: 89af1b81b5221ab1cdebc0c91d5340acc62dd330
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983974"
---
# <a name="jet_indexid-structure"></a>JET_INDEXID struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_indexid-structure"></a>JET_INDEXID struttura

La **JET_INDEXID** contiene un ID indice. Un ID indice è un hint utilizzato per accelerare la selezione dell'indice corrente [tramite JetSetCurrentIndex.](./jetsetcurrentindex-function.md) È particolarmente utile quando è presente un numero molto elevato di indici in una tabella. L'ID di indice può essere recuperato [usando JetGetIndexInfo](./jetgetindexinfo-function.md) [o JetGetTableIndexInfo.](./jetgettableindexinfo-function.md)

```cpp
    typedef struct tagJET_INDEXID {
      unsigned long cbStruct;
      char rgbIndexId[sizeof(JET_API_PRT) + sizeof(unsigned long) + sizeof(unsigned long)];
    } JET_INDEXID;
```

### <a name="members"></a>Membri

**cbStruct**

Dimensione, in byte, dell'ID indice.

Si tratta delle dimensioni effettive dell'ID di indice restituito nel buffer di output da [JetGetIndexInfo](./jetgetindexinfo-function.md) [o JetGetTableIndexInfo.](./jetgettableindexinfo-function.md)

**rgbIndexId**

BLOB opaco di informazioni utilizzato dal motore per identificare rapidamente un indice nella cache dello schema.

Non tentare di interpretare il BLOB di informazioni. Non è una dimensione impostata.

### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)  
[JetSetCurrentIndex](./jetsetcurrentindex-function.md)
