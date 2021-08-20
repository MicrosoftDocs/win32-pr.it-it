---
title: Uso di messaggi finestra per gestire la Waveform-Audio riproduzione
description: Uso di messaggi finestra per gestire la Waveform-Audio riproduzione
ms.assetid: 217968fd-4bb3-405d-a371-c129e29637ab
keywords:
- audio waveform, gestione della riproduzione con i messaggi
- interfaccia audio waveform, gestione della riproduzione con i messaggi
- riproduzione di file audio waveform, gestione della riproduzione con messaggi
- audio waveform, messaggi
- interfaccia audio waveform, messaggi
- riproduzione di file audio waveform, messaggi
- MM_WOM_CLOSE messaggio
- MM_WOM_DONE messaggio
- MM_WOM_OPEN messaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a31d8a88cb74953a1d38285a77b18ac25cd7495c3e29e71c5259551b5c2c3453
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135886"
---
# <a name="using-window-messages-to-manage-waveform-audio-playback"></a>Uso di messaggi finestra per gestire la Waveform-Audio riproduzione

I messaggi seguenti possono essere inviati a una funzione di routine della finestra per la gestione della riproduzione audio waveform.



| Message                                | Descrizione                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ WOM \_ CLOSE**](mm-wom-close.md) | Inviato quando il dispositivo viene chiuso usando la [**funzione waveOutClose.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose)                                 |
| [**MM \_ WOM \_ DONE**](mm-wom-done.md)   | Inviato quando il driver di dispositivo termina con un blocco di dati inviato usando la [**funzione waveOutWrite.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) |
| [**MM \_ WOM \_ OPEN**](mm-wom-open.md)   | Inviato quando il dispositivo viene aperto usando la [**funzione waveOutOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)                                   |



 

Un *parametro wParam* *e lParam* è associato a ognuno di questi messaggi. Il *parametro wParam* specifica sempre un handle del dispositivo audio waveform aperto. Per il [**messaggio MM \_ WOM \_ DONE,**](mm-wom-done.md) *lParam* specifica un puntatore a una [**struttura WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) che identifica il blocco di dati completato. Il *parametro lParam* non viene usato per i [**messaggi MM \_ WOM \_ CLOSE**](mm-wom-close.md) e [**MM \_ WOM \_ OPEN.**](mm-wom-open.md)

Il messaggio più utile è probabilmente MM \_ WOM \_ DONE. Quando questo messaggio segnala che la riproduzione di un blocco di dati è stata completata, è possibile pulire e liberare il blocco di dati. A meno che non sia necessario allocare memoria o inizializzare variabili, probabilmente non è necessario elaborare i messaggi MM WOM OPEN e \_ \_ MM \_ WOM \_ CLOSE.

La funzione di callback per i dispositivi di output audio-waveform viene fornita dall'applicazione. Per informazioni su questa funzione di callback, vedere la [**funzione waveOutProc.**](/previous-versions//dd743869(v=vs.85))

 

 