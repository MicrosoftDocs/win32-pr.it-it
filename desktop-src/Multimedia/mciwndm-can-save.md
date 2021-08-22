---
title: MCIWNDM_CAN_SAVE messaggio (Vfw.h)
description: Il messaggio MCIWNDM \_ CAN SAVE determina se un dispositivo \_ MCI può salvare i dati. È possibile inviare questo messaggio in modo esplicito o tramite la macro MCIWndCanSave.
ms.assetid: b4e27190-b095-494b-9ed3-10653bea187b
keywords:
- MCIWNDM_CAN_SAVE messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccab622381208b8213414ed8b156a84e431afffc55acdf2323b0c0a2d31014f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429631"
---
# <a name="mciwndm_can_save-message"></a>MESSAGGIO DI MCIWNDM \_ CAN \_ SAVE

Il **messaggio MCIWNDM \_ CAN \_ SAVE** determina se un dispositivo MCI può salvare i dati. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndCanSave.**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)


```C++
MCIWNDM_CAN_SAVE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** il dispositivo supporta il salvataggio o FALSE in caso **contrario.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)
</dt> </dl>

 

 





