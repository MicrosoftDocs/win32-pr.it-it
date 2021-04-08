---
title: Messaggio di MCIWNDM_GETDEVICEID (VFW. h)
description: Il \_ messaggio MCIWNDM GETDEVICEID recupera l'identificatore del dispositivo MCI attualmente aperto da usare con la funzione mciSendCommand. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetDeviceID.
ms.assetid: 188f15fa-579a-438e-a812-9a2b684127c0
keywords:
- MCIWNDM_GETDEVICEID messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GETDEVICEID
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f2271b18dcf8f295594031ab2c7c80dd8dec06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047973"
---
# <a name="mciwndm_getdeviceid-message"></a>\_Messaggio MCIWNDM GETDEVICEID

Il messaggio **MCIWNDM \_ GETDEVICEID** recupera l'identificatore del dispositivo MCI attualmente aperto da usare con la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) . È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) .


```C++
MCIWNDM_GETDEVICEID 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce l'identificatore del dispositivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid)
</dt> </dl>

 

