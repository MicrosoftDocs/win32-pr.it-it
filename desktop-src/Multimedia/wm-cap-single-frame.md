---
title: Messaggio di WM_CAP_SINGLE_FRAME (VFW. h)
description: Il \_ messaggio con \_ frame singolo WM Cap \_ aggiunge un singolo frame a un file di acquisizione aperto con il messaggio di \_ apertura del \_ singolo frame WM Cap \_ \_ . È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capCaptureSingleFrame.
ms.assetid: 95466961-0719-4ff7-afc8-f7bf0e0974ac
keywords:
- WM_CAP_SINGLE_FRAME messaggi multimediali di Windows
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
ms.openlocfilehash: a919036ee38fdcf00f55c3d4044cd3f45bd13c82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121383"
---
# <a name="wm_cap_single_frame-message"></a>\_Messaggio con \_ frame singolo WM Cap \_

Il messaggio con **\_ \_ \_ frame singolo WM Cap** aggiunge un singolo frame a un file di acquisizione aperto con il messaggio di [**\_ \_ \_ \_ apertura del singolo frame WM Cap**](wm-cap-single-frame-open.md) . È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe) .


```C++
WM_CAP_SINGLE_FRAME 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.

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

 

 





