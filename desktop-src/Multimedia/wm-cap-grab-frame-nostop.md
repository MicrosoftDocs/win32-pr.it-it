---
title: WM_CAP_GRAB_FRAME_NOSTOP messaggio (Vfw.h)
description: Il messaggio \_ NOSTOP WM CAP GRAB FRAME riempie il buffer dei frame con un singolo frame non compresso dal dispositivo di acquisizione \_ \_ e lo \_ visualizza.
ms.assetid: 5f6e3ce7-3595-456e-82c8-eeb162ace81a
keywords:
- WM_CAP_GRAB_FRAME_NOSTOP messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME_NOSTOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b81c581ad7e3913640271b32b18791ebf7b48ed09cd365af82ed263449f05471
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622600"
---
# <a name="wm_cap_grab_frame_nostop-message"></a>Messaggio \_ \_ \_ NOSTOP DI WM CAP GRAB \_ FRAME

Il **messaggio \_ \_ \_ \_ NOSTOP WM CAP GRAB FRAME** riempie il buffer dei frame con un singolo frame non compresso dal dispositivo di acquisizione e lo visualizza. A differenza del [**messaggio WM CAP GRAB \_ \_ \_ FRAME,**](wm-cap-grab-frame.md) lo stato di sovrapposizione o anteprima non viene modificato da questo messaggio. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capGrabFrameNoStop.**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop)


```C++
WM_CAP_GRAB_FRAME_NOSTOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Per informazioni sull'installazione delle funzioni di callback, vedere i [**messaggi WM CAP SET CALLBACK \_ \_ \_ \_ ERROR**](wm-cap-set-callback-error.md) e [**WM CAP SET CALLBACK \_ \_ \_ \_ FRAME.**](wm-cap-set-callback-frame.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> <dt>

[Messaggi di acquisizione video](video-capture-messages.md)
</dt> </dl>

 

 





