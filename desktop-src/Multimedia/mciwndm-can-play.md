---
title: MCIWNDM_CAN_PLAY messaggio (Vfw.h)
description: Il messaggio MCIWNDM CAN PLAY determina se un dispositivo MCI può riprodurre un file di dati o un contenuto \_ \_ di altro tipo. È possibile inviare questo messaggio in modo esplicito o tramite la macro MCIWndCanPlay.
ms.assetid: dbb742b0-b8ab-4b80-96da-c4823a4747c9
keywords:
- MCIWNDM_CAN_PLAY messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84d067b01dbce8aaab7c78ab24c3d11fc5d4a3a19b9bfdb663eb653ebc0c553c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374243"
---
# <a name="mciwndm_can_play-message"></a>MESSAGGIO DI MCIWNDM \_ CAN \_ PLAY

Il **messaggio MCIWNDM \_ CAN \_ PLAY** determina se un dispositivo MCI può riprodurre un file di dati o un contenuto di altro tipo. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndCanPlay.**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)


```C++
MCIWNDM_CAN_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** il dispositivo supporta la riproduzione dei dati o FALSE in caso **contrario.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)
</dt> </dl>

 

 





