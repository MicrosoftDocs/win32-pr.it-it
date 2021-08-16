---
description: 'Altre informazioni su: JET_BKLOGTIME Structure'
title: JET_BKLOGTIME struttura
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
ms.openlocfilehash: b34740d582e341cce3b2fd0b28203b7346a4de1d94a8586289be8ab252247943
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118487723"
---
# <a name="jet_bklogtime-structure"></a>JET_BKLOGTIME struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_bklogtime-structure"></a>JET_BKLOGTIME struttura

La **JET_BKLOGTIME** contiene gli elementi di data e ora di un evento. È un'estensione di [JET_LOGTIME](./jet-logtime-structure.md).

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

**bSecondi**

Ora dell'evento in secondi. Può essere da 0 (zero) a 60. 0 (zero) viene usato quando la **struttura JET_BKLOGTIME** è "null".

**bMinutes**

Ora dell'evento in minuti. Può essere da 0 (zero) a 60. 0 (zero) viene usato quando la **struttura JET_BKLOGTIME** è "null".

**bHours**

Ora dell'evento in ore. Può essere da 0 (zero) a 24. 0 (zero) viene usato quando la **struttura JET_BKLOGTIME** è "null".

**Compleanno**

Giorno del mese dell'evento. Può essere da 0 (zero) a 31. 0 (zero) viene usato quando la **struttura JET_BKLOGTIME** è "null".

**bMonth**

Mese dell'anno dell'evento. Può essere da 0 (zero) a 12. 0 (zero) viene usato quando la **struttura JET_BKLOGTIME** è "null".

**bAnno**

Anno (offset di 1900) dell'evento. Per ottenere l'anno effettivo, aggiungere 1900 a questo valore. 0 (zero) viene usato quando la **struttura JET_BKLOGTIME** è "null".

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
<td><p>backup in streaming</p></td>
<td><p>0 (zero)</p></td>
</tr>
<tr class="even">
<td><p>backup snapshot</p></td>
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
<td><p>Dichiarato in Esent.h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
