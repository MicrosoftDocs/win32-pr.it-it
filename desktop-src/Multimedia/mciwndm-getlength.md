---
title: MCIWNDM_GETLENGTH messaggio (Vfw.h)
description: Il messaggio MCIWNDM GETLENGTH recupera la lunghezza del contenuto o \_ del file attualmente usato da un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o usando la macro MCIWndGetLength.
ms.assetid: bee4d9fc-78eb-4577-98bb-d6c2d9acbb7f
keywords:
- MCIWNDM_GETLENGTH di Windows multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_GETLENGTH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 334d9a4a62171a62cbd0fc914be2d9a81ed901eab6d3893170cb8dabd2426a36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374188"
---
# <a name="mciwndm_getlength-message"></a>Messaggio MCIWNDM \_ GETLENGTH

Il **messaggio MCIWNDM \_ GETLENGTH** recupera la lunghezza del contenuto o del file attualmente usato da un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o usando la macro [**MCIWndGetLength.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength)


```C++
MCIWNDM_GETLENGTH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce la lunghezza. Le unità per la lunghezza dipendono dal formato di ora corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength)
</dt> </dl>

 

 





