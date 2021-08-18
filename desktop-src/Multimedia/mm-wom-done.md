---
title: MM_WOM_DONE messaggio (Mmsystem.h)
description: Il messaggio MM \_ WOM DONE viene inviato a una finestra quando il buffer di output specificato \_ viene restituito all'applicazione. I buffer vengono restituiti all'applicazione quando sono stati riprodotti o come risultato di una chiamata alla funzione waveOutReset.
ms.assetid: bbdebb68-82e5-4963-90bb-f93f8a91a8cf
keywords:
- MM_WOM_DONE di Windows multimediali
topic_type:
- apiref
api_name:
- MM_WOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 225ba32f780831ab8b40f487a312a940219abc2e976be75a4e903648344afc89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065461"
---
# <a name="mm_wom_done-message"></a>MESSAGGIO \_ MM WOM \_ DONE

Il **messaggio MM \_ WOM \_ DONE** viene inviato a una finestra quando il buffer di output specificato viene restituito all'applicazione. I buffer vengono restituiti all'applicazione quando sono stati riprodotti o come risultato di una chiamata alla [**funzione waveOutReset.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)


```C++
MM_WOM_DONE 
wParam = (WPARAM) hOutputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*
</dt> <dd>

Handle per il dispositivo di output audio-forma d'onda che ha riprodotto il buffer.

</dd> <dt>

<span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*
</dt> <dd>

Puntatore a [**una struttura WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) che identifica il buffer.

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

 

