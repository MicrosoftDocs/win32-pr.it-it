---
description: 'Altre informazioni su: struttura JET_LOGTIME'
title: Struttura JET_LOGTIME
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
ms.openlocfilehash: 9c99e2c1f77a01c33a75d3e5d16c4fe58c122a4e
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "103762425"
---
# <a name="jet_logtime-structure"></a>Struttura JET_LOGTIME


_**Si applica a:** Windows | Windows Server_

## <a name="jet_logtime-structure"></a>Struttura JET_LOGTIME

La struttura **JET_LOGTIME** include gli elementi della data e dell'ora di un evento.

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

**bSeconds**

Ora dell'evento in secondi. Questo valore può essere compreso tra 0 e 59. 0 viene utilizzato quando la struttura è null.

**bMinutes**

Ora dell'evento in minuti. Questo valore può essere compreso tra 0 e 59. 0 viene utilizzato quando la struttura è null.

**Gabriele**

Ora dell'evento in ore. Questo valore può essere compreso tra 0 e 23. 0 viene utilizzato quando la struttura è null.

**bDay**

Giorno del mese dell'evento. Questo valore può essere compreso tra 0 e 31. 0 viene utilizzato quando la struttura è null.

**bMonth**

Mese dell'anno dell'evento. Questo valore può essere compreso tra 0 e 12. 0 viene utilizzato quando la struttura è null.

**bYear**

Anno dell'evento (offset di 1900). Per ottenere l'anno effettivo, aggiungere 1900 a questo valore. 0 viene utilizzato quando la struttura è null.

**bFiller1**

Questo campo deve essere ignorato.

**fTimeIsUTC**

L'ora è in formato UTC.

**fUnused**

Questo campo deve essere ignorato.

**bFiller2**

Questo campo deve essere ignorato.

### <a name="remarks"></a>Commenti

Questa struttura è destinata principalmente all'uso nel debug.

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

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
