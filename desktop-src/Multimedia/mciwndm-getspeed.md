---
title: MCIWNDM_GETSPEED messaggio (Vfw.h)
description: Il messaggio GETSPEED DI MCIWNDM \_ recupera la velocità di riproduzione di un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o tramite la macro MCIWndGetSpeed.
ms.assetid: d10a8f88-e85e-449b-8655-bb0832031d59
keywords:
- MCIWNDM_GETSPEED messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_GETSPEED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42749fb2f99c446dbd45bc6e2497287ab3b0ce987c9343ed4580735c760cc892
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429251"
---
# <a name="mciwndm_getspeed-message"></a>MESSAGGIO GETSPEED DI MCIWNDM \_

Il **messaggio \_ GETSPEED DI MCIWNDM** recupera la velocità di riproduzione di un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndGetSpeed.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed)


```C++
MCIWNDM_GETSPEED 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce la velocità di riproduzione in caso di esito positivo. Il valore per la velocità normale è 1000. I valori più grandi indicano velocità più veloci, valori più piccoli indicano velocità più lente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed)
</dt> </dl>

 

 





