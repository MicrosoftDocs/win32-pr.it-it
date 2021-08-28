---
title: MCIWNDM_CAN_EJECT messaggio (Vfw.h)
description: Il messaggio MCIWNDM \_ CAN \_ EJECT determina se un dispositivo MCI può espellere i supporti. È possibile inviare questo messaggio in modo esplicito o tramite la macro MCIWndCanEject.
ms.assetid: e9bd33c4-0ad8-4c0a-8b75-52011b58904d
keywords:
- MCIWNDM_CAN_EJECT messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fde4c9fec3972fe0e22b0a562454e1ef680e9ccae3851c272d28468fc2c91f74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429671"
---
# <a name="mciwndm_can_eject-message"></a>MCIWNDM \_ PUÒ \_ INVIARE UN MESSAGGIO

Il **messaggio MCIWNDM \_ CAN \_ EJECT** determina se un dispositivo MCI può espellere i supporti. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndCanEject.**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)


```C++
MCIWNDM_CAN_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** il dispositivo può rimuovere il supporto o FALSE in caso **contrario.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)
</dt> </dl>

 

 





