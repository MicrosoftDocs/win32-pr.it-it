---
title: WOM_DONE messaggio (Mmsystem.h)
description: Il messaggio WOM DONE viene inviato a una funzione di callback di output waveform-audio quando il buffer di output specificato \_ viene restituito all'applicazione.
ms.assetid: cac94a44-d1b0-43de-b3ec-ae34547b1fc3
keywords:
- WOM_DONE messaggio Windows multimediali
topic_type:
- apiref
api_name:
- WOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f8e54fe6f8f79c9fe5885861dbda758a663ca49b38ed559b06ba59627768055
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134816"
---
# <a name="wom_done-message"></a>Messaggio WOM \_ DONE

Il **messaggio WOM \_ DONE** viene inviato a una funzione di callback di output waveform-audio quando il buffer di output specificato viene restituito all'applicazione. I buffer vengono restituiti all'applicazione quando sono stati riprodotti o come risultato di una chiamata alla [**funzione waveOutReset.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)


```C++
WOM_DONE 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Puntatore a [**una struttura WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) che identifica il buffer.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Riservato; deve essere zero.

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

[Messaggi waveform](waveform-messages.md)
</dt> </dl>

 

