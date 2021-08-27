---
description: 'Altre informazioni su: JET_LOGTIME Structure'
title: JET_LOGTIME struttura
TOCTitle: JET_LOGTIME Structure
ms:assetid: cb7c0b74-db7a-4e48-80b8-37b3fdf6d088
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294089(v=EXCHG.10)
ms:contentKeyID: 32765704
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
ms.openlocfilehash: 9cb6fac65451518e20dd64ee223638165ac5c752
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470476"
---
# <a name="jet_logtime-structure"></a>JET_LOGTIME struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_logtime-structure"></a>JET_LOGTIME struttura

La **JET_LOGTIME** contiene elementi della data e dell'ora di un evento.

```cpp
typedef struct {
  char bSeconds;
  char bMinutes;
  char bHours;
  char bDay;
  char bMonth;
  char bYear;
  union {
    char bFiller1;
    struct {
        unsigned char fTimeIsUTC: 1;
        unsigned char fUnused: 7;
    };
  };
  char bFiller2;
} JET_LOGTIME;
```

### <a name="members"></a>Membri

**bSecondi**

Ora dell'evento in secondi. Questo valore può essere compreso tra 0 e 59. Quando la struttura è Null, viene usato 0.

**bMinutes**

Ora dell'evento in minuti. Questo valore può essere compreso tra 0 e 59. Quando la struttura è Null, viene usato 0.

**bHours**

Ora dell'evento in ore. Questo valore può essere compreso tra 0 e 23. Quando la struttura è Null, viene usato 0.

**Compleanno**

Giorno del mese dell'evento. Questo valore può essere compreso tra 0 e 31. Quando la struttura è Null, viene usato 0.

**bMonth**

Mese dell'anno dell'evento. Questo valore può essere compreso tra 0 e 12. Quando la struttura è Null, viene usato 0.

**bAnno**

Anno dell'evento (offset per 1900). Per ottenere l'anno effettivo, aggiungere 1900 a questo valore. Quando la struttura è Null, viene usato 0.

**bFiller1**

Questo campo deve essere ignorato.

**fTimeIsUTC**

L'ora è in formato UTC.

**fUnused**

Questo campo deve essere ignorato.

**bFiller2**

Questo campo deve essere ignorato.

### <a name="remarks"></a>Commenti

Questa struttura è destinata principalmente all'utilizzo nel debug.

### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
