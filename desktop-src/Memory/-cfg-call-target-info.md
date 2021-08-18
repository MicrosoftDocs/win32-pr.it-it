---
description: Rappresenta informazioni sulle destinazioni di chiamata per Control Flow Guard (CFG).
ms.assetid: 8DEF907F-3F23-4122-95CE-F413FC7FD96B
title: CFG_CALL_TARGET_INFO struttura (Ntmmapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFG_CALL_TARGET_INFO
api_type:
- HeaderDef
api_location:
- ntmmapi.h
ms.openlocfilehash: e3bd7d351e890a968f2fa01ddffa6c8e3be16164d78393894055f55660c516bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040281"
---
# <a name="cfg_call_target_info-structure"></a>Struttura CFG \_ CALL \_ TARGET \_ INFO

Rappresenta informazioni sulle destinazioni di chiamata per Control Flow Guard (CFG).

## <a name="syntax"></a>Sintassi


```C++
typedef struct _CFG_CALL_TARGET_INFO {
  ULONG_PTR Offset;
  ULONG_PTR Flags;
} CFG_CALL_TARGET_INFO, *PCFG_CALL_TARGET_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**Offset**
</dt> <dd>

Offset relativo a un indirizzo virtuale specificato (iniziale). Questo offset deve essere allineato a 16 byte.

</dd> <dt>

**Flag**
</dt> <dd>

Flag che descrivono l'operazione da eseguire sull'indirizzo. Se **CFG \_ CALL TARGET \_ \_ VALID** è impostato, l'indirizzo verrà contrassegnato come valido per CFG. In caso contrario, verrà contrassegnata come destinazione di chiamata non valida.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                          |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Ntmmapi.h</dt> </dl> |



 

 




