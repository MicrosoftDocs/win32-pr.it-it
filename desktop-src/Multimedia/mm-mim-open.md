---
title: Messaggio MM_MIM_OPEN (mmsystem. h)
description: Il \_ \_ messaggio di apertura mm MIM viene inviato a una finestra quando viene aperto un dispositivo di input MIDI.
ms.assetid: 8dfc24a0-0ab8-4f49-954f-0c0a55fa28bc
keywords:
- MM_MIM_OPEN messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_MIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7d87e391336b948d0c784048baeffa7bba88b29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873269"
---
# <a name="mm_mim_open-message"></a>MM \_ \_ messaggio aperto MIM

Il messaggio di **\_ \_ apertura mm MIM** viene inviato a una finestra quando viene aperto un dispositivo di input MIDI.


```C++
MM_MIM_OPEN 
wParam = (WPARAM) hInput 
lParam = reserved 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*
</dt> <dd>

Handle per il dispositivo di input MIDI che è stato aperto.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Riservati Non usare.

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

[MIDI (Musical Instrument Digital Interface)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[Messaggi MIDI](midi-messages.md)
</dt> </dl>

 

 





