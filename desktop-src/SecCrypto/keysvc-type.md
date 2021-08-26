---
description: L'enumerazione \_ KEYSVC TYPE definisce se una chiave viene applicata a un computer o a un servizio.
ms.assetid: 573a412a-1e9d-47ac-bd09-2319d4b9712b
title: KEYSVC_TYPE enumerazione (Rkeysvcc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_TYPE
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 3c23cc259029cf76fcb1590e6261623827d59b48c9a0728e21c8250ca3e858f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119976095"
---
# <a name="keysvc_type-enumeration"></a>Enumerazione KEYSVC \_ TYPE

**L'enumerazione \_ KEYSVC TYPE** definisce se una chiave viene applicata a un computer o a un servizio.

## <a name="syntax"></a>Sintassi


```C++
typedef enum _KEYSVC_TYPE { 
  KeySvcMachine,
  KeySvcService
} KEYSVC_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="KeySvcMachine"></span><span id="keysvcmachine"></span><span id="KEYSVCMACHINE"></span>**KeySvcMachine**
</dt> <dd>

La chiave è per un computer.

</dd> <dt>

<span id="KeySvcService"></span><span id="keysvcservice"></span><span id="KEYSVCSERVICE"></span>**KeySvcService**
</dt> <dd>

La chiave è per un servizio.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Rkeysvcc.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)
</dt> </dl>

 

 




