---
title: Messaggio di MCIWNDM_SETVOLUME (VFW. h)
description: Il \_ messaggio MCIWNDM volume imposta il livello di volume di un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndSetVolume.
ms.assetid: 04151588-b761-447a-9a57-808c034c3059
keywords:
- MCIWNDM_SETVOLUME messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_SETVOLUME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2215f8df3ea6f7b36b224318ebac68175ff9c265
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740231"
---
# <a name="mciwndm_setvolume-message"></a>\_Messaggio MCIWNDM volume

Il messaggio **MCIWNDM \_ volume** imposta il livello di volume di un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) .


```C++
MCIWNDM_SETVOLUME 
wParam = 0; 
lParam = (LPARAM) (UINT) iVol; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iVol"></span><span id="ivol"></span><span id="IVOL"></span>*iVol*
</dt> <dd>

Nuovo livello di volume. Specificare 1000 per il livello di volume normale. Specificare un valore superiore per un volume più alto o un valore inferiore per un volume più silenzioso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume)
</dt> </dl>

 

 





