---
title: WM_CAP_SINGLE_FRAME_CLOSE messaggio (Vfw.h)
description: Il messaggio WM CAP SINGLE FRAME CLOSE chiude il file di acquisizione aperto dal messaggio \_ WM CAP SINGLE FRAME \_ \_ \_ \_ \_ \_ \_ OPEN. È possibile inviare questo messaggio in modo esplicito o usando la macro capCaptureSingleFrameClose.
ms.assetid: fde5f34b-0781-49a2-a509-64192a1d9ec0
keywords:
- WM_CAP_SINGLE_FRAME_CLOSE messaggio Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME_CLOSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f304fd0c62818562e53c6129a15b266db6f1ac000de64fb779e5cdb3e437d43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134965"
---
# <a name="wm_cap_single_frame_close-message"></a>Messaggio DI \_ CHIUSURA DI UN SINGOLO \_ \_ FRAME \_ WM CAP

Il **messaggio WM CAP SINGLE FRAME \_ \_ \_ \_ CLOSE** chiude il file di acquisizione aperto dal messaggio [**WM CAP SINGLE FRAME \_ \_ \_ \_ OPEN.**](wm-cap-single-frame-open.md) È possibile inviare questo messaggio in modo esplicito o usando la macro [**capCaptureSingleFrameClose.**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose)


```C++
WM_CAP_SINGLE_FRAME_CLOSE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo o FALSE **in** caso contrario.

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

 

 





