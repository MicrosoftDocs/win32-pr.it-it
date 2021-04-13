---
title: Messaggio di MCIWNDM_EJECT (VFW. h)
description: Il \_ messaggio MCIWNDM EJECT Invia un comando a un dispositivo MCI per espellerne i supporti. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndEject.
ms.assetid: a492f504-8b58-480e-9766-bc2878466c44
keywords:
- MCIWNDM_EJECT messaggi multimediali di Windows
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
ms.openlocfilehash: e41686ce41b82dc48ee6c22ac556606c79c5b24a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400356"
---
# <a name="mciwndm_eject-message"></a>\_Messaggio di espulsione MCIWNDM

Il messaggio **MCIWNDM \_ eject** Invia un comando a un dispositivo MCI per espellerne i supporti. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject) .


```C++
MCIWNDM_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject)
</dt> </dl>

 

 





