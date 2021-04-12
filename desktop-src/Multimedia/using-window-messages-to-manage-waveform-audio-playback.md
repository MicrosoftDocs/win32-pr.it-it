---
title: Uso dei messaggi della finestra per gestire Waveform-Audio la riproduzione
description: Uso dei messaggi della finestra per gestire Waveform-Audio la riproduzione
ms.assetid: 217968fd-4bb3-405d-a371-c129e29637ab
keywords:
- audio della forma d'onda, gestione della riproduzione con messaggi
- waveform-interfaccia audio, gestione della riproduzione con messaggi
- riproduzione di file audio con forma d'onda, gestione della riproduzione con messaggi
- audio Waveform, messaggi
- waveform-interfaccia audio, messaggi
- riproduzione di file audio (Waveform), messaggi
- Messaggio MM_WOM_CLOSE
- Messaggio MM_WOM_DONE
- Messaggio MM_WOM_OPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce02794222274e10498e31e0f38939d930ef3745
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337102"
---
# <a name="using-window-messages-to-manage-waveform-audio-playback"></a>Uso dei messaggi della finestra per gestire Waveform-Audio la riproduzione

I messaggi seguenti possono essere inviati a una funzione di routine della finestra per la gestione della riproduzione dell'audio e della forma d'onda.



| Message                                | Descrizione                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ WOM \_ Close**](mm-wom-close.md) | Inviato quando il dispositivo viene chiuso tramite la funzione [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) .                                 |
| [**MM \_ WOM \_ completato**](mm-wom-done.md)   | Inviato quando il driver di dispositivo viene terminato con un blocco di dati inviato tramite la funzione [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) . |
| [**MM \_ WOM \_ aperto**](mm-wom-open.md)   | Inviato quando il dispositivo viene aperto tramite la funzione [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) .                                   |



 

Un parametro *wParam* e *lParam* è associato a ognuno di questi messaggi. Il parametro *wParam* specifica sempre un handle del dispositivo waveform aperto-audio. Per il messaggio [**mm \_ WOM \_ done**](mm-wom-done.md) , *lParam* specifica un puntatore a una struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) che identifica il blocco di dati completato. Il parametro *lParam* non è utilizzato per i messaggi di [**chiusura di mm \_ \_ WOM**](mm-wom-close.md) e [**mm \_ WOM \_ aperti**](mm-wom-open.md) .

Il messaggio più utile è probabilmente MM \_ WOM \_ fatto. Quando questo messaggio segnala che la riproduzione di un blocco di dati è stata completata, è possibile pulire e liberare il blocco di dati. A meno che non sia necessario allocare memoria o inizializzare variabili, è probabile che non sia necessario elaborare i \_ messaggi di chiusura mm WOM \_ Open e mm \_ WOM \_ .

La funzione di callback per i dispositivi Waveform-Audio output viene fornita dall'applicazione. Per informazioni su questa funzione di callback, vedere la funzione [**waveOutProc**](/previous-versions//dd743869(v=vs.85)) .

 

 