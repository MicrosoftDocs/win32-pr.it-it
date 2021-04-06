---
title: Messaggio di MCIWNDM_CAN_EJECT (VFW. h)
description: MCIWNDM \_ può \_ rimuovere il messaggio determina se un dispositivo MCI può espellerne i supporti. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndCanEject.
ms.assetid: e9bd33c4-0ad8-4c0a-8b75-52011b58904d
keywords:
- MCIWNDM_CAN_EJECT messaggi multimediali di Windows
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
ms.openlocfilehash: 00ba54c9263e23fdd9830be892e4559ae3755c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743687"
---
# <a name="mciwndm_can_eject-message"></a>MCIWNDM \_ può \_ rimuovere il messaggio

**MCIWNDM \_ può \_ rimuovere** il messaggio determina se un dispositivo MCI può espellerne i supporti. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject) .


```C++
MCIWNDM_CAN_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **true** se il dispositivo può espellere il relativo supporto o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)
</dt> </dl>

 

 





