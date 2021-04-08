---
description: 'Altre informazioni su: struttura JET_RECORDLIST'
title: Struttura JET_RECORDLIST
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
ms.openlocfilehash: 16aca3a13bbae7c61bfe03aca49acea775820d39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885017"
---
# <a name="jet_recordlist-structure"></a>Struttura JET_RECORDLIST


_**Si applica a:** Windows | Windows Server_

## <a name="jet_recordlist-structure"></a>Struttura JET_RECORDLIST

La struttura **JET_RECORDLIST** trova i record che si trovano nell'intersezione degli intervalli di indice specificati quando vengono utilizzati con la funzione [JetIntersectIndexes](./jetintersectindexes-function.md) .

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

Dimensioni in byte della struttura **JET_RECORDLIST** .

**TableID**

Identificatore di tabella di una tabella temporanea che contiene i segnalibri per i risultati della query. La tabella verrà chiusa automaticamente se viene eseguito il rollback della transazione corrente con [JetRollback](./jetrollback-function.md); in caso contrario, deve essere chiuso con [JetCloseTable](./jetclosetable-function.md).

**cRecord**

Numero di righe nella tabella temporanea.

**columnidBookmark**

Identificatore di colonna della colonna del segnalibro nella tabella temporanea.

### <a name="remarks"></a>Commenti

La tabella temporanea identificata da **TableID** ha una sola colonna. Questa singola colonna include i segnalibri e ogni record deve rientrare in un buffer di dimensioni JET_cbBookmarkMost byte.

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
[JetRollback](./jetrollback-function.md)
