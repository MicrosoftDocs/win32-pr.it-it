---
title: MCIWNDM_EJECT messaggio (Vfw.h)
description: Il messaggio MCIWNDM EJECT invia un comando a un \_ dispositivo MCI per espellere i relativi supporti. È possibile inviare questo messaggio in modo esplicito o tramite la macro MCIWndEject.
ms.assetid: a492f504-8b58-480e-9766-bc2878466c44
keywords:
- MCIWNDM_EJECT messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66c752f192e8f74f2c6e861e581fd22a561bafd9ff6c0f369ba669bc4bf87fb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429431"
---
# <a name="mciwndm_eject-message"></a>Messaggio MCIWNDM \_ EJECT

Il **messaggio MCIWNDM \_ EJECT** invia un comando a un dispositivo MCI per espellere i relativi supporti. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndEject.**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject)


```C++
MCIWNDM_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject)
</dt> </dl>

 

 





