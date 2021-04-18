---
description: 'Altre informazioni su: struttura JET_BKLOGTIME'
title: Struttura JET_BKLOGTIME
TOCTitle: JET_BKLOGTIME Structure
ms:assetid: 31460079-7c5b-4145-837d-b112ba0117d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269219(v=EXCHG.10)
ms:contentKeyID: 32765522
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
ms.openlocfilehash: 0b3ebfd1c0b807a491695ba18d6735e0230a16fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316498"
---
# <a name="jet_bklogtime-structure"></a>Struttura JET_BKLOGTIME


_**Si applica a:** Windows | Windows Server_

## <a name="jet_bklogtime-structure"></a>Struttura JET_BKLOGTIME

La struttura **JET_BKLOGTIME** include gli elementi di data e ora di un evento. Si tratta di un'estensione di [JET_LOGTIME](./jet-logtime-structure.md).

**Windows Vista: JET_BKLOGTIME** è stato introdotto in Windows Vista.

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
      union {
        char bFiller2;
        struct {
          unsigned char fOSSnapshot  :1;
          unsigned char fReserved  :7;
        };
      };
    } JET_BKLOGTIME;
```

### <a name="members"></a>Membri

**bSeconds**

Ora dell'evento in secondi. Il valore può essere 0 (zero) e 60. 0 (zero) viene usato quando la struttura del **JET_BKLOGTIME** è "null".

**bMinutes**

Ora dell'evento in minuti. Il valore può essere 0 (zero) e 60. 0 (zero) viene usato quando la struttura del **JET_BKLOGTIME** è "null".

**Gabriele**

Ora dell'evento in ore. Può essere 0 (zero) a 24. 0 (zero) viene usato quando la struttura del **JET_BKLOGTIME** è "null".

**bDay**

Giorno del mese dell'evento. Può essere 0 (zero) a 31. 0 (zero) viene usato quando la struttura del **JET_BKLOGTIME** è "null".

**bMonth**

Mese dell'anno dell'evento. Può essere 0 (zero) a 12. 0 (zero) viene usato quando la struttura del **JET_BKLOGTIME** è "null".

**bYear**

Anno (offset di 1900) dell'evento. Per ottenere l'anno effettivo, aggiungere 1900 a questo valore. 0 (zero) viene usato quando la struttura del **JET_BKLOGTIME** è "null".

**bFiller1**

Questo campo deve essere ignorato.

**fTimeIsUTC**

L'ora è in formato UTC.

**fUnused**

Questo campo deve essere ignorato.

**bFiller2**

Questo campo deve essere ignorato.

**fOSSnapshot**

Se questo evento è un backup, questo flag contiene uno dei valori possibili seguenti:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Valore</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>backup di flusso</p></td>
<td><p>0 (zero)</p></td>
</tr>
<tr class="even">
<td><p>backup di snapshot</p></td>
<td><p>1</p></td>
</tr>
</tbody>
</table>


**fReserved**

Questo campo deve essere ignorato.

### <a name="remarks"></a>Commenti

Questa struttura viene utilizzata durante il debug.

### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
