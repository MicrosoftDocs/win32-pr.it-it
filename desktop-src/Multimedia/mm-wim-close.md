---
title: Messaggio MM_WIM_CLOSE (mmsystem. h)
description: Il \_ \_ messaggio di chiusura Wim mm viene inviato a una finestra quando viene chiuso un dispositivo di input audio e di forma d'onda. L'handle del dispositivo non è più valido dopo l'invio di questo messaggio.
ms.assetid: 4ea35b66-6bfa-41f0-9d52-a8cf2b0a69dd
keywords:
- MM_WIM_CLOSE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_WIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d9934ef7045debbcac2f5baf1c2f750d22dad5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047828"
---
# <a name="mm_wim_close-message"></a>\_Messaggio di \_ chiusura Wim mm

Il messaggio di **\_ \_ chiusura Wim mm** viene inviato a una finestra quando viene chiuso un dispositivo di input audio e di forma d'onda. L'handle del dispositivo non è più valido dopo l'invio di questo messaggio.


```C++
MM_WIM_CLOSE 
wParam = (WPARAM) hInputDev 
lParam = reserved 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*
</dt> <dd>

Handle per il dispositivo di input della forma d'onda-audio che è stato chiuso.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Riservati deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Audio Waveform](waveform-audio.md)
</dt> <dt>

[Messaggi di forma d'onda](waveform-messages.md)
</dt> </dl>

 

 





