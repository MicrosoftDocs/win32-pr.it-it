---
title: Messaggio di WM_CAP_EDIT_COPY (VFW. h)
description: Il \_ \_ messaggio di copia di modifica di WM Cap \_ copia il contenuto del buffer del frame video e della tavolozza associata negli Appunti. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capEditCopy.
ms.assetid: 16f1dd7d-af4d-4096-add8-eec5f0a0607f
keywords:
- WM_CAP_EDIT_COPY messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_EDIT_COPY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb81c21fc10846adaa113c02b6250bbb35cfff50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120451"
---
# <a name="wm_cap_edit_copy-message"></a>\_ \_ Modifica \_ copia messaggio WM Cap

Il messaggio di **\_ copia di \_ modifica \_ di WM Cap** copia il contenuto del buffer del frame video e della tavolozza associata negli Appunti. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) .


```C++
WM_CAP_EDIT_COPY 
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

 

 





