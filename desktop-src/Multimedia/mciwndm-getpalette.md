---
title: MCIWNDM_GETPALETTE messaggio (Vfw.h)
description: Il messaggio MCIWNDM \_ GETPALETTE recupera un handle della tavolozza usata da un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o tramite la macro MCIWndGetPalette.
ms.assetid: f8426344-0fee-4419-9d8a-dcee26cb4c28
keywords:
- MCIWNDM_GETPALETTE messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_GETPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 319fe1fedc21c064896c3316d0a45132c034b73c25bf107ee667269a13ed678b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137702"
---
# <a name="mciwndm_getpalette-message"></a>Messaggio MCIWNDM \_ GETPALETTE

Il **messaggio MCIWNDM \_ GETPALETTE** recupera un handle della tavolozza usata da un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndGetPalette.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette)


```C++
MCIWNDM_GETPALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce l'handle della tavolozza in caso di esito positivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette)
</dt> </dl>

 

 





