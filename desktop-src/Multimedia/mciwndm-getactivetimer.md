---
title: MCIWNDM_GETACTIVETIMER messaggio (Vfw.h)
description: Il messaggio MCIWNDM GETACTIVETIMER recupera il periodo di aggiornamento usato quando la \_ finestra MCIWnd è la finestra attiva. È possibile inviare questo messaggio in modo esplicito o usando la macro MCIWndGetActiveTimer.
ms.assetid: f9e6f9ed-75fd-4e45-ad92-79a82d8d572c
keywords:
- MCIWNDM_GETACTIVETIMER messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_GETACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bc542e5a4b43b974eb7f28bc59d8e2fab7547834f28b5bccb6ea46f978e2158
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525521"
---
# <a name="mciwndm_getactivetimer-message"></a>Messaggio MCIWNDM \_ GETACTIVETIMER

Il **messaggio MCIWNDM \_ GETACTIVETIMER** recupera il periodo di aggiornamento usato quando la finestra MCIWnd è la finestra attiva. È possibile inviare questo messaggio in modo esplicito o usando la macro [**MCIWndGetActiveTimer.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer)


```C++
MCIWNDM_GETACTIVETIMER 
wParam = 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valore restituito

Restituisce il periodo di aggiornamento in millisecondi. Il valore predefinito è 500 millisecondi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer)
</dt> </dl>

 

 





