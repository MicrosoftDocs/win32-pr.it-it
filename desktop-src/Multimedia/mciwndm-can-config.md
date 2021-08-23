---
title: MCIWNDM_CAN_CONFIG messaggio (Vfw.h)
description: Il messaggio MCIWNDM \_ CAN CONFIG determina se un dispositivo \_ MCI può visualizzare una finestra di dialogo di configurazione. È possibile inviare questo messaggio in modo esplicito o tramite la macro MCIWndCanConfig.
ms.assetid: f1eb22a8-d0fc-4d2c-a414-392e560cfbed
keywords:
- MCIWNDM_CAN_CONFIG messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_CONFIG
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef5b8e4f8e1ab09f128b1294034bbb715c834c3e867f31bbaae0cb6bd620be5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525531"
---
# <a name="mciwndm_can_config-message"></a>Messaggio DI CONFIGURAZIONE DI MCIWNDM \_ \_ CAN

Il **messaggio MCIWNDM \_ CAN \_ CONFIG** determina se un dispositivo MCI può visualizzare una finestra di dialogo di configurazione. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndCanConfig.**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig)


```C++
MCIWNDM_CAN_CONFIG 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** il dispositivo supporta la configurazione o FALSE in caso **contrario.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig)
</dt> </dl>

 

 





