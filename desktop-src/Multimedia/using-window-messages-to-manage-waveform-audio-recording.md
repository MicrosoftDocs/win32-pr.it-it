---
title: Uso dei messaggi della finestra per gestire la registrazione Waveform-Audio
description: Uso dei messaggi della finestra per gestire la registrazione Waveform-Audio
ms.assetid: 65637d51-9d30-48db-8681-48332442130e
keywords:
- audio della forma d'onda, gestione della registrazione con messaggi
- waveform-interfaccia audio, gestione della registrazione con messaggi
- registrazione dell'audio della forma d'onda, gestione della registrazione con messaggi
- audio Waveform, messaggi
- waveform-interfaccia audio, messaggi
- registrazione dell'audio della forma d'onda, messaggi
- Messaggio MM_WIM_CLOSE
- Messaggio MM_WIM_DATA
- Messaggio MM_WIM_OPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70bb1cfe1ed0f7ba6052fc1eb6af8fca8355d87d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472835"
---
# <a name="using-window-messages-to-manage-waveform-audio-recording"></a>Uso dei messaggi della finestra per gestire la registrazione Waveform-Audio

I messaggi seguenti possono essere inviati a una funzione di routine della finestra per la gestione della registrazione audio e della forma d'onda.



| Message                                | Descrizione                                                                                                                  |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**\_Wim \_ chiusura di mm**](mm-wim-close.md) | Inviato quando il dispositivo viene chiuso tramite la funzione [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose) .                                     |
| [**\_dati WIM \_ mm**](mm-wim-data.md)   | Inviato quando il driver di dispositivo viene terminato con un buffer inviato tramite la funzione [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) . |
| [**\_Wim \_ aperto mm**](mm-wim-open.md)   | Inviato quando il dispositivo viene aperto tramite la funzione [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) .                                       |



 

Il parametro *lParam* dei [**\_ \_ dati WIM mm**](mm-wim-data.md) specifica un puntatore a una struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) che identifica il buffer. Questo buffer potrebbe non essere completamente riempito con i dati audio della forma d'onda. la registrazione può arrestarsi prima del riempimento del buffer. Usare il membro **dwBytesRecorded** della struttura **WAVEHDR** per determinare la quantità di dati validi presenti nel buffer.

Il messaggio più utile è probabilmente [**i \_ \_ dati WIM mm**](mm-wim-data.md). Quando l'applicazione termina usando il blocco di dati inviato dal driver di dispositivo, è possibile pulire e liberare il blocco di dati. A meno che non sia necessario allocare memoria o inizializzare variabili, è probabile che non sia necessario usare i messaggi [**di \_ \_ chiusura**](mm-wim-close.md) WIM con formato WIM [**mm \_ \_**](mm-wim-open.md) .

La funzione di callback per i dispositivi di input audio e di forma d'onda viene fornita dall'applicazione. Per informazioni su questa funzione di callback, vedere la funzione [**waveInProc**](/previous-versions//dd743849(v=vs.85)) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione dell'audio della forma d'onda](recording-waveform-audio.md)
</dt> </dl>

 

 