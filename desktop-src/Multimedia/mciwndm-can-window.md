---
title: Messaggio di MCIWNDM_CAN_WINDOW (VFW. h)
description: Il \_ messaggio della finestra MCIWNDM può \_ determinare se un dispositivo MCI supporta i comandi MCI orientati a finestre. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndCanWindow.
ms.assetid: bf89c096-1272-441e-9334-2b4215dbc979
keywords:
- MCIWNDM_CAN_WINDOW messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_WINDOW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d638b61093483b6e834b57af1d5c892d77d0f1d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964098"
---
# <a name="mciwndm_can_window-message"></a>MCIWNDM \_ può \_ messaggio finestra

Il messaggio della **\_ \_ finestra MCIWNDM può** determinare se un dispositivo MCI supporta i comandi MCI orientati a finestre. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) .


```C++
MCIWNDM_CAN_WINDOW 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **true** se il dispositivo supporta i comandi MCI orientati alla finestra o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow)
</dt> </dl>

 

 





