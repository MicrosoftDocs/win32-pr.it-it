---
title: Messaggio di MCIWNDM_GETINACTIVETIMER (VFW. h)
description: Il \_ messaggio MCIWNDM GETINACTIVETIMER Recupera il periodo di aggiornamento usato quando la finestra di MCIWnd è la finestra inattiva. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetInactiveTimer.
ms.assetid: 84e00d2f-2cf8-4b6b-a8cb-7eb320754783
keywords:
- MCIWNDM_GETINACTIVETIMER messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a270aeffdee59b7749aa87a0e711204960d74d7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301080"
---
# <a name="mciwndm_getinactivetimer-message"></a>\_Messaggio MCIWNDM GETINACTIVETIMER

Il messaggio **MCIWNDM \_ GETINACTIVETIMER** Recupera il periodo di aggiornamento usato quando la finestra di MCIWnd è la finestra inattiva. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) .


```C++
MCIWNDM_GETINACTIVETIMER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce il periodo di aggiornamento, in millisecondi. Il valore predefinito è 2000 millisecondi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer)
</dt> </dl>

 

 





