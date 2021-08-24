---
title: MM_MOM_CLOSE messaggio (Mmsystem.h)
description: Il messaggio MM MOM CLOSE viene inviato a una finestra quando un dispositivo di \_ \_ output MIDI viene chiuso.
ms.assetid: 4829bbe5-5103-4354-88a7-37def22e926e
keywords:
- MM_MOM_CLOSE messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MM_MOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8e8c9af8f6a5fb454a2f7759b5e64804e82c568b15549d01f7478a3d7c6041d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807151"
---
# <a name="mm_mom_close-message"></a>MESSAGGIO \_ DI CHIUSURA DI MM MOM \_

Il **messaggio MM MOM \_ \_ CLOSE** viene inviato a una finestra quando un dispositivo di output MIDI viene chiuso.


```C++
MM_MOM_CLOSE 
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

## <a name="remarks"></a>Commenti

L'handle del dispositivo non è più valido dopo l'invio del messaggio.

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

 

 





