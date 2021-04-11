---
title: Messaggio di MCIWNDM_GETACTIVETIMER (VFW. h)
description: Il \_ messaggio MCIWNDM GETACTIVETIMER Recupera il periodo di aggiornamento usato quando la finestra di MCIWnd è la finestra attiva. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetActiveTimer.
ms.assetid: f9e6f9ed-75fd-4e45-ad92-79a82d8d572c
keywords:
- MCIWNDM_GETACTIVETIMER messaggi multimediali di Windows
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
ms.openlocfilehash: 4cb86fc2940c8bd5d82c004754b81e5389ada892
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121671"
---
# <a name="mciwndm_getactivetimer-message"></a>\_Messaggio MCIWNDM GETACTIVETIMER

Il messaggio **MCIWNDM \_ GETACTIVETIMER** Recupera il periodo di aggiornamento usato quando la finestra di MCIWnd è la finestra attiva. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) .


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
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer)
</dt> </dl>

 

 





