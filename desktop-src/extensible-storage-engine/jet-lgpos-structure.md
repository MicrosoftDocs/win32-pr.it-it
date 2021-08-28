---
description: 'Altre informazioni su: JET_LGPOS struttura'
title: JET_LGPOS struttura
TOCTitle: JET_LGPOS Structure
ms:assetid: dbce1a60-b32b-40c1-a215-e93bb77cd8c1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294113(v=EXCHG.10)
ms:contentKeyID: 32765727
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
ms.openlocfilehash: e3e83786236a95cf2b0c4d77e26e6987334a5b00
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986154"
---
# <a name="jet_lgpos-structure"></a>JET_LGPOS struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_lgpos-structure"></a>JET_LGPOS struttura

La **JET_LGPOS** contiene dati interni al meccanismo di registrazione del motore di database. Questa struttura è considerata interna.

```cpp
    typedef struct {
      unsigned short ib;
      unsigned short isec;
      long lGeneration;
    } JET_LGPOS;
```

### <a name="members"></a>Membri

**Ib**

Supporta l'infrastruttura ESE e non può essere usato dal codice.

**Isec**

Supporta l'infrastruttura ESE e non può essere usato dal codice.

**lGenerazione**

Supporta l'infrastruttura ESE e non può essere usato dal codice.

### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
