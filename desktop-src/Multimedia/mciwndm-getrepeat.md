---
title: MCIWNDM_GETREPEAT messaggio (Vfw.h)
description: Il messaggio MCIWNDM \_ GETREPEAT determina se è stata attivata la riproduzione continua. È possibile inviare questo messaggio in modo esplicito o usando la macro MCIWndGetRepeat.
ms.assetid: 6d644117-e705-421f-b45f-9f0e833e6bc8
keywords:
- MCIWNDM_GETREPEAT messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_GETREPEAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5045f56f2d189884e6d2dee978ec8800fa9c24c3ff01fc3fe93680b4ae7f53af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374198"
---
# <a name="mciwndm_getrepeat-message"></a>Messaggio MCIWNDM \_ GETREPEAT

Il **messaggio MCIWNDM \_ GETREPEAT** determina se è stata attivata la riproduzione continua. È possibile inviare questo messaggio in modo esplicito o usando la macro [**MCIWndGetRepeat.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat)


```C++
MCIWNDM_GETREPEAT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** la riproduzione continua è attivata o FALSE in caso **contrario.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat)
</dt> </dl>

 

 





