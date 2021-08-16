---
title: WIM_DATA messaggio (Mmsystem.h)
description: Il messaggio WIM DATA viene inviato alla funzione di callback di input audio-forma d'onda specificata quando i dati audio-forma d'onda sono presenti nel buffer di input e il buffer viene \_ restituito all'applicazione.
ms.assetid: 94cc02b8-61c4-44b9-9f8e-041fe989c1a6
keywords:
- WIM_DATA messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- WIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6956dacefa507c2c92f05afdd39bc9c803c630421c81620e0320f3b06648b13b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940749"
---
# <a name="wim_data-message"></a>Messaggio WIM \_ DATA

Il **messaggio WIM \_ DATA** viene inviato alla funzione di callback di input audio-forma d'onda specificata quando i dati audio-forma d'onda sono presenti nel buffer di input e il buffer viene restituito all'applicazione. Il messaggio può essere inviato quando il buffer è pieno o dopo la chiamata della funzione [**waveInReset.**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)


```C++
WIM_DATA 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Puntatore a [**una struttura WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) che identifica il buffer contenente i dati.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Riservato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Il buffer restituito potrebbe non essere pieno. Usare il **membro dwBytesRecorded** della struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) specificato da *lpwvhdr* per determinare il numero di byte registrati nel buffer restituito.

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

 

