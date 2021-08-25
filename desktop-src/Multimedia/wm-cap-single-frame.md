---
title: WM_CAP_SINGLE_FRAME messaggio (Vfw.h)
description: Il messaggio WM CAP SINGLE FRAME aggiunge un singolo frame a un file di acquisizione aperto usando il messaggio \_ WM CAP SINGLE FRAME \_ \_ \_ \_ \_ \_ OPEN. È possibile inviare questo messaggio in modo esplicito o usando la macro capCaptureSingleFrame.
ms.assetid: 95466961-0719-4ff7-afc8-f7bf0e0974ac
keywords:
- WM_CAP_SINGLE_FRAME messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2080c8471849d42c2260c1f4133c996ef31e65e8a20591df531fbd24c19bc85c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891791"
---
# <a name="wm_cap_single_frame-message"></a>Messaggio \_ WM CAP SINGLE \_ \_ FRAME

Il **messaggio WM CAP SINGLE \_ \_ \_ FRAME** aggiunge un singolo frame a un file di acquisizione aperto usando il messaggio [**WM CAP SINGLE FRAME \_ \_ \_ \_ OPEN.**](wm-cap-single-frame-open.md) È possibile inviare questo messaggio in modo esplicito o usando la macro [**capCaptureSingleFrame.**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe)


```C++
WM_CAP_SINGLE_FRAME 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o FALSE **in** caso contrario.

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

 

 





