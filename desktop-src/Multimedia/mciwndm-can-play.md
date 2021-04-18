---
title: Messaggio di MCIWNDM_CAN_PLAY (VFW. h)
description: MCIWNDM è in \_ grado \_ di riprodurre il messaggio determina se un dispositivo MCI può riprodurre un file di dati o un contenuto di un altro tipo. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndCanPlay.
ms.assetid: dbb742b0-b8ab-4b80-96da-c4823a4747c9
keywords:
- MCIWNDM_CAN_PLAY messaggi multimediali di Windows
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
ms.openlocfilehash: 043a0fc15260f7448df8d009a6b468616244269d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302626"
---
# <a name="mciwndm_can_play-message"></a>MCIWNDM è in \_ grado di \_ riprodurre il messaggio

MCIWNDM è in **\_ grado di \_ riprodurre** il messaggio determina se un dispositivo MCI può riprodurre un file di dati o un contenuto di un altro tipo. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay) .


```C++
MCIWNDM_CAN_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **true** se il dispositivo supporta la riproduzione dei dati o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)
</dt> </dl>

 

 





