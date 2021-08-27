---
description: 'Altre informazioni su: JET_BKLOGTIME struttura'
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
ms.openlocfilehash: 2d6f8e3f77d905eb601441ad8ab3ca88bb08f59d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478527"
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

**bSeconds**

Ora dell'evento in secondi. Può essere da 0 (zero) a 60. 0 (zero) viene usato quando la **struttura JET_BKLOGTIME** è "null".

**bMinutes**

Ora dell'evento in minuti. Può essere da 0 (zero) a 60. 0 (zero) viene usato quando la **struttura JET_BKLOGTIME** è "null".

**bHours**

Ora dell'evento in ore. Può essere da 0 (zero) a 24. 0 (zero) viene usato quando la **struttura JET_BKLOGTIME** è "null".

**Compleanno**

Giorno del mese dell'evento. Può essere da 0 (zero) a 31. 0 (zero) viene usato quando la **struttura JET_BKLOGTIME** è "null".

**bMonth**

Mese dell'anno dell'evento. Può essere da 0 (zero) a 12. 0 (zero) viene usato quando la **struttura JET_BKLOGTIME** è "null".

**bYear**

Anno (offset per 1900) dell'evento. Per ottenere l'anno effettivo, aggiungere 1900 a questo valore. 0 (zero) viene usato quando la **struttura JET_BKLOGTIME** è "null".

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


| <p>Nome</p> | <p>valore</p> | 
|-------------|--------------|
| <p>backup in streaming</p> | <p>0 (zero)</p> | 
| <p>backup di snapshot</p> | <p>1</p> | 



**fReserved**

Questo campo deve essere ignorato.

### <a name="remarks"></a>Commenti

Questa struttura viene utilizzata durante il debug.

### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
