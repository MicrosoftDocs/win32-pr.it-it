---
title: Messaggio di MCIWNDM_CAN_CONFIG (VFW. h)
description: Il messaggio di configurazione MCIWNDM \_ può \_ determinare se un dispositivo MCI può visualizzare una finestra di dialogo di configurazione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndCanConfig.
ms.assetid: f1eb22a8-d0fc-4d2c-a414-392e560cfbed
keywords:
- MCIWNDM_CAN_CONFIG messaggi multimediali di Windows
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
ms.openlocfilehash: 816a8c1dfaec6fc7d7854f8873ce05e74e4de6bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479138"
---
# <a name="mciwndm_can_config-message"></a>MCIWNDM è in \_ grado di \_ configurare il messaggio

Il messaggio di configurazione **MCIWNDM \_ può \_** determinare se un dispositivo MCI può visualizzare una finestra di dialogo di configurazione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) .


```C++
MCIWNDM_CAN_CONFIG 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **true** se il dispositivo supporta la configurazione o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig)
</dt> </dl>

 

 





