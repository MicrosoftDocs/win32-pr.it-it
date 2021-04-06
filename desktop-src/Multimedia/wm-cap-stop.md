---
title: Messaggio di WM_CAP_STOP (VFW. h)
description: Il messaggio di arresto di WM \_ Cap \_ interrompe l'operazione di acquisizione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capCaptureStop.
ms.assetid: 0fea82f5-f381-485a-82ae-b081b3a5e402
keywords:
- WM_CAP_STOP messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ded89ea8999fa2b29f576a6d047f5147d492bc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743538"
---
# <a name="wm_cap_stop-message"></a>Messaggio di arresto del \_ Cap WM \_

Il messaggio di **\_ \_ arresto di WM Cap** interrompe l'operazione di acquisizione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) .

In Step Frame Capture i dati dell'immagine raccolti prima dell'invio del messaggio vengono conservati nel file di acquisizione. Se è stata abilitata l'acquisizione audio, nel file di acquisizione viene mantenuta anche una durata equivalente dei dati audio.


```C++
WM_CAP_STOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Per utilizzare questo messaggio, è necessario che l'operazione di acquisizione venga restituita. Usare il messaggio [**WM \_ Cap \_ Abort**](wm-cap-abort.md) per abbandonare l'operazione di acquisizione corrente.

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

 

 





