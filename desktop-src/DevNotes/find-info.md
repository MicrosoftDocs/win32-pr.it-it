---
description: Contiene informazioni sul contesto di ricerca.
ms.assetid: 4b865563-98c2-459b-bb2b-75420d51d6a7
title: FIND_INFO struttura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIND_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1ee5eb66928322019a455c78d71abf5461e56b1296ae79d94b83c40c2d45379e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404784"
---
# <a name="find_info-structure"></a>Struttura FIND \_ INFO

Contiene informazioni sul contesto di ricerca.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _FIND_INFO {
  TAGID     tiIndex;
  TAGID     tiCurrent;
  TAGID     tiEndIndex;
  TAG       tName;
  DWORD     dwIndexRec;
  DWORD     dwFlags;
  ULONGLONG ullKey;
  union {
    LPCTSTR szName;
    DWORD   dwName;
    GUID    *pguidName;
  };
} FIND_INFO, *PFIND_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**tiIndex**
</dt> <dd>

**TAGID per** l'indice in cui eseguire la ricerca.

</dd> <dt>

**tiCurrent**
</dt> <dd>

**TAGID per** l'elemento corrente individuato.

</dd> <dt>

**tiEndIndex**
</dt> <dd>

**TAGID per** l'ultimo record dopo FindFirst se l'indice è UNIQUE.

</dd> <dt>

**tName**
</dt> <dd>

Tipo dell'elemento da trovare. Vedere [Tipi DI TAG.](tag-types.md)

</dd> <dt>

**dwIndexRec**
</dt> <dd>

Contatore interno utilizzato per tenere traccia del punto in cui deve iniziare l'operazione di ricerca successiva nell'indice.

</dd> <dt>

**dwFlags**
</dt> <dd>

Questo membro può essere 0 o **SHIMDB \_ INDEX \_ UNIQUE \_ KEY** (0x00000001), che indica che si tratta di un indice di chiave univoca.

</dd> <dt>

**ullKey**
</dt> <dd>

Chiave per la voce corrente.

</dd> <dt>

**Szname**
</dt> <dd>

Stringa corrente (se il tipo di tag è **TAG \_ TYPE \_ STRINGREF).**

</dd> <dt>

**dwName**
</dt> <dd>

Valore **DWORD corrente** (se il tipo di tag è **TAG TYPE \_ \_ DWORD).**

</dd> <dt>

**pguidName**
</dt> <dd>

Valore GUID corrente (se il tipo di tag è **TAG \_ TYPE \_ BINARY** e TAG è **TAG DATABASE \_ \_ ID**).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbFindFirstDWORDIndexedTag**](sdbfindfirstdwordindexedtag.md)
</dt> </dl>

 

 




