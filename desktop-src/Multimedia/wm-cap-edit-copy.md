---
title: WM_CAP_EDIT_COPY messaggio (Vfw.h)
description: Il messaggio WM CAP EDIT COPY copia il contenuto del buffer dei fotogrammi video e \_ \_ della tavolozza \_ associata negli Appunti. È possibile inviare questo messaggio in modo esplicito o tramite la macro capEditCopy.
ms.assetid: 16f1dd7d-af4d-4096-add8-eec5f0a0607f
keywords:
- WM_CAP_EDIT_COPY messaggio Windows Multimediali
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
ms.openlocfilehash: e944273ff8519aefa52803b2072199760a480e0fcb2a76dd314b578dcbcfdf4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892081"
---
# <a name="wm_cap_edit_copy-message"></a>Messaggio \_ DI MODIFICA DELLA COPIA \_ \_ DI WM CAP

Il **messaggio WM CAP EDIT \_ \_ \_ COPY** copia il contenuto del buffer dei fotogrammi video e della tavolozza associata negli Appunti. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**capEditCopy.**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy)


```C++
WM_CAP_EDIT_COPY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo o FALSE **in** caso contrario.

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

 

 





