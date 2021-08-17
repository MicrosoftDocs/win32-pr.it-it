---
title: MCIWNDM_GETZOOM messaggio (Vfw.h)
description: Il messaggio MCIWNDM \_ GETZOOM recupera il valore di zoom corrente usato da un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o usando la macro MCIWndGetZoom.
ms.assetid: 92db8df2-515a-4616-a0f5-245d466ba379
keywords:
- MCIWNDM_GETZOOM messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_GETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52c247230ffe6269f77b906d874a4cf82a21ed8d3388ffa18193417603e45fbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374142"
---
# <a name="mciwndm_getzoom-message"></a>Messaggio MCIWNDM \_ GETZOOM

Il **messaggio MCIWNDM \_ GETZOOM** recupera il valore di zoom corrente usato da un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o usando la macro [**MCIWndGetZoom.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom)


```C++
MCIWNDM_GETZOOM 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce i valori più recenti usati con [**MCIWNDM \_ SETZOOM.**](mciwndm-setzoom.md)

## <a name="remarks"></a>Commenti

Un valore restituito pari a 100 indica che l'immagine non è ingrandita. Il valore 200 indica che l'immagine viene ingrandita al doppio delle dimensioni originali. Il valore 50 indica che l'immagine è ridotta a metà delle dimensioni originali.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom)
</dt> <dt>

[**MCIWNDM \_ SETZOOM**](mciwndm-setzoom.md)
</dt> </dl>

 

 





