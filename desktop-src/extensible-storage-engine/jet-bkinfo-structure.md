---
description: 'Altre informazioni su: JET_BKINFO struttura'
title: JET_BKINFO struttura
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
ms.openlocfilehash: 477c84ee0b466fb43ee0bb06ef14a2a1be6dd00e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472187"
---
# <a name="jet_bkinfo-structure"></a>JET_BKINFO struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_bkinfo-structure"></a>JET_BKINFO struttura

La **JET_BKINFO** contiene una raccolta di dati relativi a un evento di backup specifico.

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

ID del backup.

**logtimeMark**

Ora di questo evento di backup.

**bklogtimeMark**

Ora di questo evento di backup, con bit aggiuntivi per indicare un backup dello snapshot.

**Windows Vista: bklogtimeMark** è stato introdotto in Windows Vista.

**genLow**

Numero di generazione del log basso associato a questo evento di backup.

**genHigh**

Numero elevato di generazione del log associato a questo evento di backup.

### <a name="remarks"></a>Commenti

Questa struttura viene utilizzata all'interno [della JET_DBINFOMISC](./jet-dbinfomisc-structure.md) per rappresentare i dati relativi all'evento di backup del database.

### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_BKLOGTIME](./jet-bklogtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
