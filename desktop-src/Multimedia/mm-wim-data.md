---
title: MM_WIM_DATA messaggio (Mmsystem.h)
description: Il messaggio MM WIM DATA viene inviato a una finestra quando i dati audio waveform sono presenti nel buffer di input e il buffer viene \_ \_ restituito all'applicazione. Il messaggio può essere inviato quando il buffer è pieno o dopo la chiamata della funzione waveInReset.
ms.assetid: 14298153-ea2f-40b7-bca7-196f4e6c1155
keywords:
- MM_WIM_DATA messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MM_WIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8b209e59032c0da4c875a316008c889cf064ae7d8bc48f5c621125a06582673
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065471"
---
# <a name="mm_wim_data-message"></a>Messaggio MM \_ WIM \_ DATA

Il **messaggio MM \_ WIM \_ DATA** viene inviato a una finestra quando i dati audio waveform sono presenti nel buffer di input e il buffer viene restituito all'applicazione. Il messaggio può essere inviato quando il buffer è pieno o dopo la chiamata della funzione [**waveInReset.**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)


```C++
MM_WIM_DATA 
wParam = (WPARAM) hInputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*
</dt> <dd>

Handle per il dispositivo di input audio-forma d'onda che ha ricevuto i dati.

</dd> <dt>

<span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*
</dt> <dd>

Puntatore a [**una struttura WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) che identifica il buffer contenente i dati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Il buffer restituito potrebbe non essere pieno. Usare il **membro dwBytesRecorded** della struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) specificato da *lParam* per determinare il numero di byte registrati nel buffer restituito.

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

 

