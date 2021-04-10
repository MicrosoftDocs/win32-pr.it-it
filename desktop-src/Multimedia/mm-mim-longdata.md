---
title: Messaggio MM_MIM_LONGDATA (mmsystem. h)
description: Il \_ \_ messaggio LONGDATA in mm MIM viene inviato a una finestra quando viene ricevuto un messaggio esclusivo del sistema MIDI completo o quando un buffer è stato riempito con dati esclusivi del sistema.
ms.assetid: 72b9eade-4224-436f-bfef-32204eaf51ae
keywords:
- MM_MIM_LONGDATA messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_MIM_LONGDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25bf1900ef2e9394b9d8772747eba873f8d607f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121254"
---
# <a name="mm_mim_longdata-message"></a>MM \_ \_ messaggio LONGDATA MIM

Il **messaggio \_ \_ LONGDATA in mm MIM** viene inviato a una finestra quando viene ricevuto un messaggio esclusivo del sistema MIDI completo o quando un buffer è stato riempito con dati esclusivi del sistema.


```C++
MM_MIM_LONGDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*
</dt> <dd>

Handle per il dispositivo di input MIDI che ha ricevuto i dati.

</dd> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Puntatore a una struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) che identifica il buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Il buffer restituito potrebbe non essere pieno. Per determinare il numero di byte registrati nel buffer restituito, usare il membro **dwBytesRecorded** della struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) a cui punta *lpMidiHdr*.

Nessun timestamp disponibile con questo messaggio. Per i dati di input con timestamp, è necessario utilizzare i messaggi inviati alle funzioni di callback.

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

 

