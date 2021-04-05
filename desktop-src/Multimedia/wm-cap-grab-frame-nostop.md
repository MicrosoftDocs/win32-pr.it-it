---
title: Messaggio di WM_CAP_GRAB_FRAME_NOSTOP (VFW. h)
description: Il \_ \_ messaggio NOSTOP di WM Cap \_ \_ Capture frame riempie il frame buffer con un singolo frame non compresso dal dispositivo di acquisizione e lo Visualizza.
ms.assetid: 5f6e3ce7-3595-456e-82c8-eeb162ace81a
keywords:
- WM_CAP_GRAB_FRAME_NOSTOP messaggi multimediali di Windows
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
ms.openlocfilehash: 5073cf5eae44f564d24cd1ebb67193d8738fd77b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874293"
---
# <a name="wm_cap_grab_frame_nostop-message"></a>\_ \_ \_ Messaggio NOSTOP frame di cattura WM Cap \_

Il **messaggio \_ \_ \_ \_ NOSTOP di WM Cap Capture frame** riempie il frame buffer con un singolo frame non compresso dal dispositivo di acquisizione e lo Visualizza. A differenza del messaggio [**di \_ \_ cattura del \_ frame WM Cap**](wm-cap-grab-frame.md) , lo stato della sovrimpressione o dell'anteprima non viene modificato da questo messaggio. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) .


```C++
WM_CAP_GRAB_FRAME_NOSTOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Per informazioni sull'installazione delle funzioni di callback, vedere l' [**errore di callback di WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) e [**WM \_ Cap \_ set callback message \_ \_ frame**](wm-cap-set-callback-frame.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> <dt>

[Messaggi di acquisizione video](video-capture-messages.md)
</dt> </dl>

 

 





