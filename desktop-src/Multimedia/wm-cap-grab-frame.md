---
title: WM_CAP_GRAB_FRAME messaggio (Vfw.h)
description: Il messaggio WM \_ CAP GRAB FRAME recupera e visualizza un singolo frame dal driver di \_ \_ acquisizione. Dopo l'acquisizione, la sovrapposizione e l'anteprima sono disabilitate. È possibile inviare questo messaggio in modo esplicito o usando la macro capGrabFrame.
ms.assetid: 91d58c1c-53b9-4813-88c2-7a1acf641d96
keywords:
- WM_CAP_GRAB_FRAME messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdccfc9df0f3abac7febfa78029b4ecb351ec3044c618dc4c811e91b433f0f49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892041"
---
# <a name="wm_cap_grab_frame-message"></a>Messaggio \_ WM CAP GRAB \_ \_ FRAME

Il **messaggio WM CAP GRAB \_ \_ \_ FRAME** recupera e visualizza un singolo frame dal driver di acquisizione. Dopo l'acquisizione, la sovrapposizione e l'anteprima sono disabilitate. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capGrabFrame.**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe)


```C++
WM_CAP_GRAB_FRAME 
wParam = (WPARAM)0; 
lParam = (LPARAM)0L; 
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

 

 





