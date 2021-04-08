---
title: Messaggio MM_WOM_DONE (mmsystem. h)
description: Il \_ messaggio mm WOM \_ Done viene inviato a una finestra quando il buffer di output specificato viene restituito all'applicazione. I buffer vengono restituiti all'applicazione quando vengono riprodotti o come risultato di una chiamata alla funzione waveOutReset.
ms.assetid: bbdebb68-82e5-4963-90bb-f93f8a91a8cf
keywords:
- MM_WOM_DONE messaggi multimediali di Windows
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
ms.openlocfilehash: 7198aa2f60a7f5a0e6d839a3ee5b453a3a4d3f59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743914"
---
# <a name="mm_wom_done-message"></a>MM \_ WOM \_ fatto messaggio

Il messaggio **mm \_ WOM \_ done** viene inviato a una finestra quando il buffer di output specificato viene restituito all'applicazione. I buffer vengono restituiti all'applicazione quando vengono riprodotti o come risultato di una chiamata alla funzione [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) .


```C++
MM_WOM_DONE 
wParam = (WPARAM) hOutputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*
</dt> <dd>

Handle per il dispositivo di output waveform-audio che ha riprodotto il buffer.

</dd> <dt>

<span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*
</dt> <dd>

Puntatore a una struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) che identifica il buffer.

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

 

