---
title: MM_WOM_OPEN messaggio (Mmsystem.h)
description: Il messaggio MM \_ WOM OPEN viene inviato a una finestra quando viene aperto il dispositivo di output \_ audio-forma d'onda specificato.
ms.assetid: 1b0366de-61cd-4203-9173-ababaefdb153
keywords:
- MM_WOM_OPEN messaggio Windows Multimedia
topic_type:
- apiref
api_name:
- MM_WOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e770d03b847352152846d1095bc528bff8e8eacbcdbb1c9fc46450d21dc185bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065401"
---
# <a name="mm_wom_open-message"></a>Messaggio MM \_ WOM \_ OPEN

Il **messaggio MM \_ WOM \_ OPEN** viene inviato a una finestra quando viene aperto il dispositivo di output audio-forma d'onda specificato.


```C++
MM_WOM_OPEN 
wParam = (WPARAM) hOutputDev 
lParam = reserved 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*
</dt> <dd>

Handle per il dispositivo aperto.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Riservato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Waveform Audio](waveform-audio.md)
</dt> <dt>

[Messaggi Waveform](waveform-messages.md)
</dt> </dl>

 

 





