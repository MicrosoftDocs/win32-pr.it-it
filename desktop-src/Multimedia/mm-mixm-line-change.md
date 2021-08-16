---
title: MM_MIXM_LINE_CHANGE messaggio (Mmsystem.h)
description: Il messaggio MM MIXM LINE CHANGE viene inviato da un dispositivo mixer per notificare a un'applicazione che lo stato di una linea audio nel \_ \_ dispositivo specificato è \_ cambiato. L'applicazione deve aggiornare la visualizzazione e i valori memorizzati nella cache per la linea audio specificata.
ms.assetid: 68ada0be-9dc5-4edf-b924-ef0d10a1b79a
keywords:
- MM_MIXM_LINE_CHANGE messaggio Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIXM_LINE_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed3bd1c122d5e0cf62aa39266da547cd3701e43e6afbf01b853c7d24040504d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373580"
---
# <a name="mm_mixm_line_change-message"></a>MM \_ MIXM \_ LINE CHANGE \_ message

Il **messaggio MM \_ MIXM LINE \_ \_ CHANGE** viene inviato da un dispositivo mixer per notificare a un'applicazione che lo stato di una linea audio nel dispositivo specificato è cambiato. L'applicazione deve aggiornare la visualizzazione e i valori memorizzati nella cache per la linea audio specificata.


```C++
MM_MIXM_LINE_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwLineID 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*
</dt> <dd>

Handle per il dispositivo mixer che ha inviato il messaggio di notifica.

</dd> <dt>

<span id="dwLineID"></span><span id="dwlineid"></span><span id="DWLINEID"></span>*dwLineID*
</dt> <dd>

Identificatore di riga per la riga audio che ha modificato lo stato. Questo identificatore corrisponde al membro **dwLineID** della struttura **MIXERLINE** restituito dalla **funzione mixerGetLineInfo.**

</dd> </dl>

## <a name="remarks"></a>Commenti

Un'applicazione deve aprire un dispositivo mixer e specificare una finestra di callback per ricevere il **messaggio MM \_ MIXM LINE \_ \_ CHANGE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Mixer audio](audio-mixers.md)
</dt> <dt>

[Messaggi Mixer audio](audio-mixer-messages.md)
</dt> </dl>

 

 





