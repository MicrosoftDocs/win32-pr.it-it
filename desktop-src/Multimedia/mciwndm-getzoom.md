---
title: Messaggio di MCIWNDM_GETZOOM (VFW. h)
description: Il \_ messaggio MCIWNDM getzoom Recupera il valore di zoom corrente usato da un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetZoom.
ms.assetid: 92db8df2-515a-4616-a0f5-245d466ba379
keywords:
- MCIWNDM_GETZOOM messaggi multimediali di Windows
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
ms.openlocfilehash: fcb4ae1883787f1b86dcc17f2d4a3e0e0ee29ced
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476228"
---
# <a name="mciwndm_getzoom-message"></a>\_Messaggio GETZOOM MCIWNDM

Il messaggio **MCIWNDM \_ getzoom** Recupera il valore di zoom corrente usato da un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) .


```C++
MCIWNDM_GETZOOM 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce i valori più recenti utilizzati con [**MCIWNDM \_ sezoom**](mciwndm-setzoom.md).

## <a name="remarks"></a>Commenti

Il valore restituito 100 indica che l'immagine non è ingrandita. Il valore 200 indica che l'immagine viene ingrandita in base al doppio delle dimensioni originali. Il valore 50 indica che l'immagine è ridotta a metà delle dimensioni originali.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom)
</dt> <dt>

[**MCIWNDM- \_ Zoom**](mciwndm-setzoom.md)
</dt> </dl>

 

 





