---
title: Messaggio di MCIWNDM_SETOWNER (VFW. h)
description: Il \_ messaggio SEtowner MCIWNDM imposta la finestra per ricevere i messaggi di notifica associati alla finestra di MCIWnd. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndSetOwner.
ms.assetid: c2d0f9d5-bf60-4036-a613-65ba1ed83110
keywords:
- MCIWNDM_SETOWNER messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_SETOWNER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3989632e83a65cda5e805bd91da3f502ca387d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120463"
---
# <a name="mciwndm_setowner-message"></a>\_Messaggio SEtowner MCIWNDM

Il **messaggio \_ SetOwner MCIWNDM** imposta la finestra per ricevere i messaggi di notifica associati alla finestra di MCIWnd. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) .


```C++
MCIWNDM_SETOWNER 
wParam = (WPARAM) hwndP; 
lParam = 0; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hwndP"></span><span id="hwndp"></span><span id="HWNDP"></span>*hwndP*
</dt> <dd>

Handle per la finestra per ricevere i messaggi di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner)
</dt> </dl>

 

 





