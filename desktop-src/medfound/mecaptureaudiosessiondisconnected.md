---
description: Inviato da un'origine di acquisizione audio quando la dessione audio viene disconnessa perché l'utente si è disconnesso da una sessione di Terminale Windows Services (WTS).
ms.assetid: 88B24E79-FEB8-46AF-9A6C-3FB426089584
title: Evento MECaptureAudioSessionDisconnected (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 567df4839776ecacb5e25992f5f8cef4795186cffc53fb8abb433418066f3c40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114171"
---
# <a name="mecaptureaudiosessiondisconnected-event"></a>Evento MECaptureAudioSessionDisconnected

Inviato da un'origine di acquisizione audio quando la dessione audio viene disconnessa perché l'utente si è disconnesso da una sessione di Terminale Windows Services (WTS).

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE               | Descrizione                           |
|-----------------------|---------------------------------------|
| VT \_ EMPTY <br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo evento viene inviato dal flusso multimediale dell'origine di acquisizione audio.

L'origine di acquisizione invia questo evento quando riceve un evento [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) dalla sessione audio con il motivo di disconnessione uguale a **DisconnectReasonSessionDisconnected.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                               |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> </dl>

 

 
