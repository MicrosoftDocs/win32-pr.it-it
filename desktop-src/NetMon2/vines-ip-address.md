---
description: La struttura degli \_ indirizzi IP delle viti \_ è un indirizzo IP in una rete VINES.
ms.assetid: 681753a5-08a2-48e6-9e46-c028c12ad9c1
title: Struttura VINES_IP_ADDRESS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VINES_IP_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c198c8c109d5aa5b841272173966ec7d9fd22299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346296"
---
# <a name="vines_ip_address-structure"></a>Struttura degli \_ indirizzi IP delle viti \_

La struttura degli **\_ \_ indirizzi IP delle viti** è un indirizzo IP in una rete VINES.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _VINES_IP_ADDRESS {
  DWORD NetID;
  WORD  SubnetID;
} VINES_IP_ADDRESS, *LPVINES_IP_ADDRESS;
```



## <a name="members"></a>Members

<dl> <dt>

**NetID**
</dt> <dd>

Identificatore di un computer specifico in una subnet specifica.

</dd> <dt>

**SubnetID**
</dt> <dd>

Identificatore di una subnet specifica sull'intera rete.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




