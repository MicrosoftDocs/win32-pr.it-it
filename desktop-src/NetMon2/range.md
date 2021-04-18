---
description: La struttura di intervallo definisce un intervallo di valori di proprietà validi.
ms.assetid: 7bd14410-f5c1-487b-8776-405567991e5a
title: Struttura RANGE (Netmon. h)
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
ms.openlocfilehash: bf465636f315e60e43350bb370e2002b8a96e635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310959"
---
# <a name="range-structure"></a>Struttura di intervallo

La struttura di **intervallo** definisce un intervallo di valori di proprietà validi.

## <a name="syntax"></a>Sintassi


```C++
typedef struct range {
  DWORD MinValue;
  DWORD MaxValue;
} RANGE, *LPRANGE;
```



## <a name="members"></a>Members

<dl> <dt>

**MinValue**
</dt> <dd>

Valore minimo possibile in un intervallo.

</dd> <dt>

**MaxValue**
</dt> <dd>

Valore massimo possibile in un intervallo.

</dd> </dl>

## <a name="remarks"></a>Commenti

La struttura di **intervallo** viene utilizzata per specificare un intervallo di numeri validi per una proprietà del protocollo. Se il membro **dataqualifier** della struttura **PropertyInfo** è impostato su **prop \_ qual \_ Range**, il membro **lpRange** della struttura [PropertyInfo](propertyinfo.md) deve fornire un puntatore a una struttura di **intervallo** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> </dl>

 

 




