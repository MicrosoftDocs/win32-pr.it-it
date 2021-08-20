---
title: Uso dei messaggi finestra per gestire la Waveform-Audio registrazione
description: Uso dei messaggi finestra per gestire la Waveform-Audio registrazione
ms.assetid: 65637d51-9d30-48db-8681-48332442130e
keywords:
- audio waveform, gestione della registrazione con messaggi
- interfaccia audio waveform,gestione della registrazione con i messaggi
- registrazione di audio waveform, gestione della registrazione con i messaggi
- audio waveform, messaggi
- interfaccia audio waveform, messaggi
- registrazione di audio waveform, messaggi
- MM_WIM_CLOSE messaggio
- MM_WIM_DATA messaggio
- MM_WIM_OPEN messaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c709df27be25a8a3f4c5a9be6528e28b4e8bab9251b04b6c397a7ef3fc8efd9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135653"
---
# <a name="using-window-messages-to-manage-waveform-audio-recording"></a>Uso dei messaggi finestra per gestire la Waveform-Audio registrazione

I messaggi seguenti possono essere inviati a una funzione di routine della finestra per la gestione della registrazione audio waveform.



| Message                                | Descrizione                                                                                                                  |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ WIM \_ CLOSE**](mm-wim-close.md) | Inviato quando il dispositivo viene chiuso usando la [**funzione waveInClose.**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose)                                     |
| [**MM \_ WIM \_ DATA**](mm-wim-data.md)   | Inviato quando il driver di dispositivo termina con un buffer inviato usando la [**funzione waveInAddBuffer.**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) |
| [**MM \_ WIM \_ OPEN**](mm-wim-open.md)   | Inviato quando il dispositivo viene aperto usando la [**funzione waveInOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen)                                       |



 

Il *parametro lParam* di [**MM \_ WIM \_ DATA**](mm-wim-data.md) specifica un puntatore a una [**struttura WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) che identifica il buffer. Questo buffer potrebbe non essere completamente riempito con dati audio waveform; la registrazione può essere interrotta prima che il buffer venga riempito. Usare il **membro dwBytesRecorded** della **struttura WAVEHDR** per determinare la quantità di dati validi presenti nel buffer.

Il messaggio più utile è probabilmente [**MM \_ WIM \_ DATA**](mm-wim-data.md). Quando l'applicazione termina di usare il blocco di dati inviato dal driver di dispositivo, è possibile pulire e liberare il blocco di dati. A meno che non sia necessario allocare memoria o inizializzare variabili, probabilmente non è necessario usare i messaggi [**MM \_ WIM \_ OPEN**](mm-wim-open.md) e [**MM \_ WIM \_ CLOSE.**](mm-wim-close.md)

La funzione di callback per i dispositivi di input audio-waveform viene fornita dall'applicazione. Per informazioni su questa funzione di callback, vedere la [**funzione waveInProc.**](/previous-versions//dd743849(v=vs.85))

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione dell'audio Waveform](recording-waveform-audio.md)
</dt> </dl>

 

 