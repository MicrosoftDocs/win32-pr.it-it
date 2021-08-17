---
title: MCIWNDM_CAN_RECORD messaggio (Vfw.h)
description: Il messaggio CAN RECORD MCIWNDM \_ determina se un dispositivo \_ MCI supporta la registrazione. È possibile inviare questo messaggio in modo esplicito o tramite la macro MCIWndCanRecord.
ms.assetid: b5a789fa-6a88-487d-a374-8f4798ee5a62
keywords:
- MCIWNDM_CAN_RECORD messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_RECORD
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5df46ce0cbffe17f890e50159a13a93192e67f60e323d6ba711bee6af7ac3f79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429651"
---
# <a name="mciwndm_can_record-message"></a>MESSAGGIO CAN RECORD MCIWNDM \_ \_

Il **messaggio CAN \_ \_ RECORD MCIWNDM** determina se un dispositivo MCI supporta la registrazione. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndCanRecord.**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord)


```C++
MCIWNDM_CAN_RECORD 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** il dispositivo supporta la registrazione o FALSE in caso **contrario.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord)
</dt> </dl>

 

 





