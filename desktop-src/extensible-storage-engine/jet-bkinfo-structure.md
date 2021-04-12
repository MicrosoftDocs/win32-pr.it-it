---
description: 'Altre informazioni su: struttura JET_BKINFO'
title: Struttura JET_BKINFO
TOCTitle: JET_BKINFO Structure
ms:assetid: dfaf1d72-1d5f-4777-91c1-6affb735b092
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294120(v=EXCHG.10)
ms:contentKeyID: 32765734
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
ms.openlocfilehash: 6c4849c23e742657d8f5eaba8a030426f7a2a440
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233374"
---
# <a name="jet_bkinfo-structure"></a>Struttura JET_BKINFO


_**Si applica a:** Windows | Windows Server_

## <a name="jet_bkinfo-structure"></a>Struttura JET_BKINFO

La struttura **JET_BKINFO** include una raccolta di dati relativi a un evento di backup specifico.

```cpp
    typedef struct {
      JET_LGPOS lgposMark;
      union {
        JET_LOGTIME logtimeMark;
        JET_BKLOGTIME bklogtimeMark;
      };
      unsigned long genLow;
      unsigned long genHigh;
    } JET_BKINFO;
```

### <a name="members"></a>Membri

**lgposMark**

ID di questo backup.

**logtimeMark**

Ora di questo evento di backup.

**bklogtimeMark**

Ora di questo evento di backup, con ulteriori bit per indicare un backup di snapshot.

**Windows Vista: bklogtimeMark** è stato introdotto in Windows Vista.

**genLow**

Numero di generazione del log basso associato a questo evento di backup.

**genHigh**

Numero di generazione del log elevato associato a questo evento di backup.

### <a name="remarks"></a>Commenti

Questa struttura viene utilizzata all'interno della struttura [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) per rappresentare i dati relativi all'evento di backup del database.

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

[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_BKLOGTIME](./jet-bklogtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
