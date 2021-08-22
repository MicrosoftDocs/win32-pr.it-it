---
title: WTSLISTENERNAME (WtsApi32.h)
description: Rappresenta il nome di un Servizi Desktop remoto listener in un server Desktop remoto Host sessione Desktop remoto.
ms.assetid: 3C41F507-6A67-4244-860F-E89B0F9E33B0
ms.tgt_platform: multiple
keywords:
- WTSLISTENERNAMEW
- WTSLISTENERNAMEA
- WTSLISTENERNAME
- PWTSLISTENERNAME
- WTSLISTENERNAME
- PWTSLISTENERNAME
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce0df52229670cd090dd900dda3c2284437297bedc25c69f12c980b9cc40d92c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513841"
---
# <a name="wtslistenername"></a>WTSLISTENERNAME

Rappresenta il nome di un Servizi Desktop remoto listener in un server Desktop remoto Host sessione Desktop remoto.


```C++
typedef WCHAR WTSLISTENERNAMEW[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEW;
typedef CHAR WTSLISTENERNAMEA[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEA;
#if UNICODE
typedef WTSLISTENERNAMEW WTSLISTENERNAME;
typedef PWTSLISTENERNAMEW PWTSLISTENERNAME;
#else 
typedef WTSLISTENERNAMEA WTSLISTENERNAME;
typedef PWTSLISTENERNAMEA PWTSLISTENERNAME;
#endif 
```



<dl> <dt>

**WTSLISTENERNAMEW**
</dt> <dd>

Nome Unicode del listener.

</dd> <dt>

**WTSLISTENERNAMEA**
</dt> <dd>

Puntatore al nome ANSI del listener.

</dd> <dt>

**WTSLISTENERNAME**
</dt> <dd>

Nome del listener.

</dd> <dt>

**PWTSLISTENERNAME**
</dt> <dd>

Puntatore al nome del listener.

</dd> <dt>

**WTSLISTENERNAME**
</dt> <dd>

Nome del listener.

</dd> <dt>

**PWTSLISTENERNAME**
</dt> <dd>

Puntatore al nome del listener.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>WtsApi32.h</dt> </dl> |



 

 





