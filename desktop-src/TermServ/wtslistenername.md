---
title: WTSLISTENERNAME (WtsApi32. h)
description: Rappresenta il nome di un listener di Servizi Desktop remoto su un server di host sessione Desktop remoto (host sessione Desktop remoto).
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
ms.openlocfilehash: a82576fc9f4490b133916852441c50dcf77e849d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400771"
---
# <a name="wtslistenername"></a>WTSLISTENERNAME

Rappresenta il nome di un listener di Servizi Desktop remoto su un server di host sessione Desktop remoto (host sessione Desktop remoto).


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
| Intestazione<br/>                   | <dl> <dt>WtsApi32. h</dt> </dl> |



 

 





