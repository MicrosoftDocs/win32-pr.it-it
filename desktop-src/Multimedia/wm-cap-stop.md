---
title: WM_CAP_STOP messaggio (Vfw.h)
description: Il messaggio WM \_ CAP \_ STOP arresta l'operazione di acquisizione. È possibile inviare questo messaggio in modo esplicito o tramite la macro capCaptureStop.
ms.assetid: 0fea82f5-f381-485a-82ae-b081b3a5e402
keywords:
- WM_CAP_STOP messaggio Windows Multimedia
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
ms.openlocfilehash: 8bceac7a821a42227a388de6ebc2b9ea548156ec80d1e5baba7f1e1ad708002d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369330"
---
# <a name="wm_cap_stop-message"></a>Messaggio \_ CAP \_ STOP WM

Il **messaggio WM CAP \_ \_ STOP** arresta l'operazione di acquisizione. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**capCaptureStop.**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop)

Nell'acquisizione dei frame del passaggio, i dati dell'immagine raccolti prima dell'invio del messaggio vengono mantenuti nel file di acquisizione. Una durata equivalente dei dati audio viene mantenuta anche nel file di acquisizione se è stata abilitata l'acquisizione audio.


```C++
WM_CAP_STOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo o FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

L'operazione di acquisizione deve cedere per utilizzare questo messaggio. Usare il [**messaggio WM \_ CAP \_ ABORT**](wm-cap-abort.md) per abbandonare l'operazione di acquisizione corrente.

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

 

 





