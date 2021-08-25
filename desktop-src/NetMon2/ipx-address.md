---
description: La struttura \_ IPX ADDRESS fornisce un indirizzo a livello di protocollo IPX.
ms.assetid: 06939ac3-3718-4441-b2c8-c73adfe3babe
title: IPX_ADDRESS struttura (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPX_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0fc8298f2495029d63889fd5ebb24cdb284933897a9d9150b1dfcc2e14084f46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743011"
---
# <a name="ipx_address-structure"></a>Struttura \_ IPX ADDRESS

La **struttura \_ IPX ADDRESS** fornisce un indirizzo a livello di protocollo IPX.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _IPX_ADDRESS {
  BYTE Subnet[4];
  BYTE Address[6];
} IPX_ADDRESS, *LPIPX_ADDRESS;
```



## <a name="members"></a>Members

<dl> <dt>

**Subnet**
</dt> <dd>

Identificatore della subnet di rete.

</dd> <dt>

**Indirizzo**
</dt> <dd>

Identificatore della scheda di interfaccia di rete della subnet.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




