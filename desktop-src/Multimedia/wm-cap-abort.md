---
title: Messaggio di WM_CAP_ABORT (VFW. h)
description: Il \_ messaggio WM Cap \_ Abort interrompe l'operazione di acquisizione.
ms.assetid: a0479d73-8422-4833-9e8a-c262ec386f58
keywords:
- WM_CAP_ABORT messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_ABORT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2843e3c4d59b62f2b58be20cef63ed0dc2e79d4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517722"
---
# <a name="wm_cap_abort-message"></a>Messaggio di interruzione di WM \_ Cap \_

Il messaggio **WM \_ Cap \_ Abort** interrompe l'operazione di acquisizione. Nel caso di Step Capture, i dati dell'immagine raccolti fino al punto del messaggio di **\_ \_ interruzione di WM Cap** verranno conservati nel file di acquisizione, ma l'audio non verrà acquisito. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) .


```C++
WM_CAP_ABORT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Per utilizzare questo messaggio, è necessario che l'operazione di acquisizione venga restituita.

Usare il messaggio di [**\_ \_ arresto di WM Cap**](wm-cap-stop.md) per arrestare l'acquisizione del passaggio nella posizione corrente e quindi acquisire l'audio.

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

 

 





