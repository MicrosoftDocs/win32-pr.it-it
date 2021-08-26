---
description: La struttura PROPERTYINSTEX definisce un'istanza di proprietà estesa in formato libero.
ms.assetid: a2316baf-07e2-4617-bb35-e20cfb11fbcb
title: Struttura PROPERTYINSTEX (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINSTEX
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 533169a98d17c56a32df56f77c30d403d0dbb28c6a51159debc9692a505da52b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036971"
---
# <a name="propertyinstex-structure"></a>Struttura PROPERTYINSTEX

La **struttura PROPERTYINSTEX** definisce un'istanza di proprietà estesa in formato libero.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PROPERTYINSTEX {
  WORD    Length;
  WORD    LengthEx;
  ULPVOID lpData;
  union {
    BYTE          Byte[];
    WORD          Word[];
    DWORD         Dword[];
    LARGE_INTEGER LargeInt[];
    SYSTEMTIME    SysTime[];
    TYPED_STRING  TypedString;
  };
} PROPERTYINSTEX;
```



## <a name="members"></a>Members

<dl> <dt>

**Length**
</dt> <dd>

Lunghezza dei dati in byte.

</dd> <dt>

**LengthEx**
</dt> <dd>

Lunghezza dei dati estesi.

</dd> <dt>

**lpData**
</dt> <dd>

Puntatore ai dati estesi.

</dd> <dt>

**Byte**
</dt> <dd>

Puntatore ai **dati BYTE.**

</dd> <dt>

**Word**
</dt> <dd>

Puntatore ai **dati WORD.**

</dd> <dt>

**Dword**
</dt> <dd>

Puntatore ai **dati DWORD.**

</dd> <dt>

**LargeInt**
</dt> <dd>

Puntatore ai **dati LARGEINT.**

</dd> <dt>

**SysTime**
</dt> <dd>

Puntatore ai **dati SYSTEMTIME.**

</dd> <dt>

**TypedString**
</dt> <dd>

Stringa tipiata che può contenere dati estesi.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




