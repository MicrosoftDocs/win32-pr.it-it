---
title: WM_CAP_ABORT messaggio (Vfw.h)
description: Il messaggio WM \_ CAP \_ ABORT arresta l'operazione di acquisizione.
ms.assetid: a0479d73-8422-4833-9e8a-c262ec386f58
keywords:
- WM_CAP_ABORT messaggio Windows Multimediali
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
ms.openlocfilehash: 904edb47c371ee13ed3492fd9257e3933bf2f001010d7dd2b0177a7729500813
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800658"
---
# <a name="wm_cap_abort-message"></a>Messaggio WM \_ CAP \_ ABORT

Il **messaggio WM CAP \_ \_ ABORT** arresta l'operazione di acquisizione. Nel caso dell'acquisizione passaggio, i dati dell'immagine raccolti fino al punto del messaggio **WM \_ CAP \_ ABORT** verranno mantenuti nel file di acquisizione, ma l'audio non verrà acquisito. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**capCaptureAbort.**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort)


```C++
WM_CAP_ABORT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo o FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

L'operazione di acquisizione deve cedere per utilizzare questo messaggio.

Usare il [**messaggio WM \_ CAP \_ STOP**](wm-cap-stop.md) per interrompere l'acquisizione dei passaggi nella posizione corrente e quindi acquisire l'audio.

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

 

 





