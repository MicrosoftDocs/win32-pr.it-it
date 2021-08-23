---
title: MCIWNDM_SETVOLUME messaggio (Vfw.h)
description: Il messaggio MCIWNDM \_ SETVOLUME imposta il livello di volume di un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o tramite la macro MCIWndSetVolume.
ms.assetid: 04151588-b761-447a-9a57-808c034c3059
keywords:
- MCIWNDM_SETVOLUME messaggio Windows Multimediali
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
ms.openlocfilehash: e8c40d2c8b2c7c4cb309b5c6e5b21dcd29e6c8ee27b9ca8c97556cb14927a121
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428541"
---
# <a name="mciwndm_setvolume-message"></a>Messaggio MCIWNDM \_ SETVOLUME

Il **messaggio MCIWNDM \_ SETVOLUME imposta** il livello di volume di un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndSetVolume.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume)


```C++
MCIWNDM_SETVOLUME 
wParam = 0; 
lParam = (LPARAM) (UINT) iVol; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iVol"></span><span id="ivol"></span><span id="IVOL"></span>*iVol*
</dt> <dd>

Nuovo livello di volume. Specificare 1000 per il livello di volume normale. Specificare un valore più alto per un volume più alto o un valore inferiore per un volume più silenzioso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume)
</dt> </dl>

 

 





