---
description: Rappresenta le informazioni sulle destinazioni di chiamata per la protezione del flusso di controllo (CFG).
ms.assetid: 8DEF907F-3F23-4122-95CE-F413FC7FD96B
title: Struttura CFG_CALL_TARGET_INFO (Ntmmapi. h)
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
ms.openlocfilehash: 66177f6b478264a10c1ce0e50297d943a16407c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311746"
---
# <a name="cfg_call_target_info-structure"></a>\_Struttura delle \_ informazioni di destinazione della chiamata cfg \_

Rappresenta le informazioni sulle destinazioni di chiamata per la protezione del flusso di controllo (CFG).

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

Offset relativo a un indirizzo virtuale (iniziale) fornito. Questo offset deve essere allineato a 16 byte.

</dd> <dt>

**Flag**
</dt> <dd>

Flag che descrivono l'operazione da eseguire sull'indirizzo. Se è impostata la **\_ destinazione della chiamata cfg \_ \_ valida** , l'indirizzo verrà contrassegnato come valido per cfg. In caso contrario, verrà contrassegnata come destinazione di chiamata non valida.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Ntmmapi. h</dt> </dl> |



 

 




