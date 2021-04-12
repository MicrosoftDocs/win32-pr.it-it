---
description: La \_ struttura dell'indirizzo IPX fornisce un indirizzo a livello di protocollo IPX.
ms.assetid: 06939ac3-3718-4441-b2c8-c73adfe3babe
title: Struttura IPX_ADDRESS (Netmon. h)
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
ms.openlocfilehash: 18645a455e780020037384a2df7173a019d71677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525867"
---
# <a name="ipx_address-structure"></a>\_Struttura di indirizzi IPX

La struttura dell' **\_ indirizzo IPX** fornisce un indirizzo a livello di protocollo IPX.

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

Identificatore NIC subnet.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




