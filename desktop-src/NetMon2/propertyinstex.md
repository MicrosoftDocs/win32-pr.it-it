---
description: La struttura PROPERTYINSTEX definisce un'istanza di proprietà estesa a mano libera.
ms.assetid: a2316baf-07e2-4617-bb35-e20cfb11fbcb
title: Struttura PROPERTYINSTEX (Netmon. h)
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
ms.openlocfilehash: f7b196d30e96f9d047f7f923d969d65a918aa4f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306481"
---
# <a name="propertyinstex-structure"></a>Struttura PROPERTYINSTEX

La struttura **PROPERTYINSTEX** definisce un'istanza di proprietà estesa a mano libera.

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

Puntatore ai dati **byte** .

</dd> <dt>

**Word**
</dt> <dd>

Puntatore ai dati di **Word** .

</dd> <dt>

**DWORD**
</dt> <dd>

Puntatore ai dati **DWORD** .

</dd> <dt>

**LargeInt**
</dt> <dd>

Puntatore ai dati **largeInt** .

</dd> <dt>

**SysTime**
</dt> <dd>

Puntatore ai dati di **SYSTEMTIME** .

</dd> <dt>

**TypedString**
</dt> <dd>

Stringa tipizzata che può avere dati estesi.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




