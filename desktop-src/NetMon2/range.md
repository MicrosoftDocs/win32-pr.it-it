---
description: La struttura RANGE definisce un intervallo di valori di proprietà validi.
ms.assetid: 7bd14410-f5c1-487b-8776-405567991e5a
title: Struttura RANGE (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RANGE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0e0135a6210aebbca38bfdede00231315dd2680461f366930b24925eda830604
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063721"
---
# <a name="range-structure"></a>Struttura RANGE

La **struttura RANGE** definisce un intervallo di valori di proprietà validi.

## <a name="syntax"></a>Sintassi


```C++
typedef struct range {
  DWORD MinValue;
  DWORD MaxValue;
} RANGE, *LPRANGE;
```



## <a name="members"></a>Members

<dl> <dt>

**Minvalue**
</dt> <dd>

Valore minimo possibile in un intervallo.

</dd> <dt>

**Maxvalue**
</dt> <dd>

Valore massimo possibile in un intervallo.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **struttura RANGE** viene usata per specificare un intervallo di numeri valido per una proprietà del protocollo. Se il **membro DataQualifier** della struttura **PROPERTYINFO** è impostato su **PROP QUAL \_ \_ RANGE,** il membro **lpRange** della [struttura PROPERTYINFO](propertyinfo.md) deve fornire un puntatore a una **struttura RANGE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Propertyinfo](propertyinfo.md)
</dt> </dl>

 

 




