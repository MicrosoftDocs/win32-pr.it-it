---
description: Contiene informazioni sul contesto di ricerca.
ms.assetid: 4b865563-98c2-459b-bb2b-75420d51d6a7
title: Struttura FIND_INFO
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
ms.openlocfilehash: 7d6b6dea42c008178c22f6e342a64b2f8d193ec5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304500"
---
# <a name="find_info-structure"></a>TROVA \_ struttura info

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

**TagId** per l'indice in cui eseguire la ricerca.

</dd> <dt>

**tiCurrent**
</dt> <dd>

**TagId** per l'elemento corrente che è stato individuato.

</dd> <dt>

**tiEndIndex**
</dt> <dd>

**TagId** per l'ultimo record dopo FindFirst se l'indice è univoco.

</dd> <dt>

**tName**
</dt> <dd>

Tipo dell'elemento da trovare. Vedere [tipi di tag](tag-types.md).

</dd> <dt>

**dwIndexRec**
</dt> <dd>

Contatore interno utilizzato per tenere traccia della posizione nell'indice in cui dovrebbe iniziare l'operazione di ricerca successiva.

</dd> <dt>

**dwFlags**
</dt> <dd>

Questo membro può essere 0 o **la \_ \_ \_ chiave univoca dell'indice SHIMDB** (0x00000001), che indica che si tratta di un indice di chiave univoca.

</dd> <dt>

**ullKey**
</dt> <dd>

Chiave per la voce corrente.

</dd> <dt>

**szName**
</dt> <dd>

Stringa corrente (se il tipo di tag è **il \_ tipo \_ di tag STRINGREF**).

</dd> <dt>

**dwName**
</dt> <dd>

Valore **DWORD** corrente (se il tipo di tag è **il \_ tipo \_ di tag DWORD**).

</dd> <dt>

**pguidName**
</dt> <dd>

Il valore GUID corrente (se il tipo di tag è un tipo di tag **\_ \_ Binary** e il tag è **tag \_ database \_ ID**).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbFindFirstDWORDIndexedTag**](sdbfindfirstdwordindexedtag.md)
</dt> </dl>

 

 




