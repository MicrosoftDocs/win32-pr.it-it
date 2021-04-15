---
title: Messaggio di MCIWNDM_CAN_SAVE (VFW. h)
description: Il MCIWNDM \_ può \_ salvare il messaggio determina se un dispositivo MCI può salvare i dati. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndCanSave.
ms.assetid: b4e27190-b095-494b-9ed3-10653bea187b
keywords:
- MCIWNDM_CAN_SAVE messaggi multimediali di Windows
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
ms.openlocfilehash: 11b60b8a5d93ac80befc8beeb6665399efe44f1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475682"
---
# <a name="mciwndm_can_save-message"></a>MCIWNDM \_ consente di \_ salvare il messaggio

Il **MCIWNDM \_ può \_ salvare** il messaggio determina se un dispositivo MCI può salvare i dati. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) .


```C++
MCIWNDM_CAN_SAVE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce **true** se il dispositivo supporta il salvataggio o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)
</dt> </dl>

 

 





