---
description: 'Altre informazioni su: JET_RECORDLIST struttura'
title: JET_RECORDLIST struttura
TOCTitle: JET_RECORDLIST Structure
ms:assetid: 6b4d97a0-4b42-4f7c-bb18-b6db3c92668a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269287(v=EXCHG.10)
ms:contentKeyID: 32765579
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
ms.openlocfilehash: e83145f74d5edf97658fdadc62f018a151ee8b55
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988229"
---
# <a name="jet_recordlist-structure"></a>JET_RECORDLIST struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_recordlist-structure"></a>JET_RECORDLIST struttura

La **JET_RECORDLIST** trova i record che si trovano nell'intersezione degli intervalli di indici specificati quando vengono usati con la [funzione JetIntersectIndexes.](./jetintersectindexes-function.md)

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidBookmark;
    } JET_RECORDLIST;
```

### <a name="members"></a>Membri

**cbStruct**

Dimensioni della struttura **JET_RECORDLIST,** in byte.

**tableid**

Identificatore di tabella di una tabella temporanea che contiene i segnalibri per i risultati della query. La tabella verrà chiusa automaticamente se viene eseguito il rollback della transazione corrente [con JetRollback](./jetrollback-function.md). In caso contrario, deve essere chiuso con [JetCloseTable.](./jetclosetable-function.md)

**cRecord**

Numero di righe nella tabella temporanea.

**columnidBookmark**

Identificatore di colonna della colonna segnalibro nella tabella temporanea.

### <a name="remarks"></a>Commenti

La tabella temporanea identificata da **tableid** include una singola colonna. Tale singola colonna contiene segnalibri e ogni record deve essere contenuto in un buffer di dimensioni JET_cbBookmarkMost byte.

### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetIntersectIndexes](./jetintersectindexes-function.md)  
[JetRollback](./jetrollback-function.md)
