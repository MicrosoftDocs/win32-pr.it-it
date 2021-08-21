---
title: MM_MOM_OPEN messaggio (Mmsystem.h)
description: Il messaggio \_ MM MOM OPEN viene inviato a una finestra quando viene aperto un dispositivo di output \_ MIDI.
ms.assetid: 1374a07c-02fa-4b43-82df-cbd96302aec5
keywords:
- MM_MOM_OPEN messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MM_MOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 842eaeeb6e18e6623f8c88d8f5c65527db36ee8370c48a4cb26edca55f6d5f5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065491"
---
# <a name="mm_mom_open-message"></a>Messaggio \_ MM MOM \_ OPEN

Il **messaggio MM MOM \_ \_ OPEN** viene inviato a una finestra quando viene aperto un dispositivo di output MIDI.


```C++
MM_MOM_OPEN 
wParam = (WPARAM) hOutput 
lParam = reserved 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*
</dt> <dd>

Handle per il dispositivo di output MIDI.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Riservato; non utilizzare .

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

[Messaggi MIDI](midi-messages.md)
</dt> </dl>

 

 





