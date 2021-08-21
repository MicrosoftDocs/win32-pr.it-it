---
title: WM_CAP_SINGLE_FRAME_OPEN messaggio (Vfw.h)
description: Il messaggio WM \_ CAP SINGLE FRAME OPEN apre il file di acquisizione per \_ \_ \_ l'acquisizione a frame singolo. Eventuali informazioni precedenti nel file di acquisizione vengono sovrascritte. È possibile inviare questo messaggio in modo esplicito o usando la macro capCaptureSingleFrameOpen.
ms.assetid: 4814737c-4395-4c01-a68e-fac43dd291fd
keywords:
- WM_CAP_SINGLE_FRAME_OPEN di Windows multimediali
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a58df70bea8971e10a769efbbc98220c46897ff6979e66ab45ae8f2ba81b971
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134836"
---
# <a name="wm_cap_single_frame_open-message"></a>Messaggio WM \_ CAP \_ SINGLE FRAME \_ \_ OPEN

Il **messaggio WM CAP SINGLE FRAME \_ \_ \_ \_ OPEN** apre il file di acquisizione per l'acquisizione a frame singolo. Eventuali informazioni precedenti nel file di acquisizione vengono sovrascritte. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capCaptureSingleFrameOpen.**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen)


```C++
WM_CAP_SINGLE_FRAME_OPEN 
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

 

 





