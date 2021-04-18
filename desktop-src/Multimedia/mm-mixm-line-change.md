---
title: Messaggio MM_MIXM_LINE_CHANGE (mmsystem. h)
description: Il \_ messaggio di modifica della riga MIXM mm \_ \_ viene inviato da un dispositivo mixer per notificare a un'applicazione che lo stato di una linea audio sul dispositivo specificato è stato modificato. L'applicazione deve aggiornare i valori visualizzati e memorizzati nella cache per la riga audio specificata.
ms.assetid: 68ada0be-9dc5-4edf-b924-ef0d10a1b79a
keywords:
- MM_MIXM_LINE_CHANGE messaggi multimediali di Windows
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
ms.openlocfilehash: 92c4aa10d9934f8cf5f5747ecb4e4eb736af2655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302024"
---
# <a name="mm_mixm_line_change-message"></a>MIXM MM- \_ \_ messaggio di \_ modifica riga

Il messaggio di **\_ \_ \_ modifica della riga MIXM mm** viene inviato da un dispositivo mixer per notificare a un'applicazione che lo stato di una linea audio sul dispositivo specificato è stato modificato. L'applicazione deve aggiornare i valori visualizzati e memorizzati nella cache per la riga audio specificata.


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

Identificatore di riga per la linea audio con stato modificato. Questo identificatore corrisponde al membro **dwLineID** della struttura **MIXERLINE** restituita dalla funzione **mixerGetLineInfo**.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un'applicazione deve aprire un dispositivo mixer e specificare una finestra di callback per ricevere il messaggio di **\_ \_ \_ modifica della riga MIXM mm** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Mixer audio](audio-mixers.md)
</dt> <dt>

[Messaggi mixer audio](audio-mixer-messages.md)
</dt> </dl>

 

 





