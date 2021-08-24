---
description: La struttura VINES \_ IP ADDRESS è un indirizzo IP in una rete \_ Vines.
ms.assetid: 681753a5-08a2-48e6-9e46-c028c12ad9c1
title: VINES_IP_ADDRESS struttura (Netmon.h)
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
ms.openlocfilehash: 23a590679fd2b4a147a8bc0f92a4d4c7b4afb8c746526de9fba7cfc388e4e1c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742201"
---
# <a name="vines_ip_address-structure"></a>Struttura DI \_ INDIRIZZI IP \_ VINES

La **struttura VINES \_ IP \_ ADDRESS** è un indirizzo IP in una rete Vines.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _VINES_IP_ADDRESS {
  DWORD NetID;
  WORD  SubnetID;
} VINES_IP_ADDRESS, *LPVINES_IP_ADDRESS;
```



## <a name="members"></a>Members

<dl> <dt>

**Netid**
</dt> <dd>

Identificatore di un computer specifico in una subnet specifica.

</dd> <dt>

**SubnetID**
</dt> <dd>

Identificatore di una subnet specifica nell'intera rete.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




