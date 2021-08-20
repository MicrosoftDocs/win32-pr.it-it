---
title: Gestione della Waveform-Audio registrazione
description: Gestione della Waveform-Audio registrazione
ms.assetid: a44f7c33-54d6-4ba7-bc57-b63c8b205392
keywords:
- audio waveform, registrazione
- interfaccia audio-forma d'onda, registrazione
- registrazione di audio waveform, about
- Struttura WAVEHDR
- Funzione waveInAddBuffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d798cb1b6a8a22f4c695bced89dd669346ad2bb6452179df1d3278af8681aa49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138934"
---
# <a name="managing-waveform-audio-recording"></a>Gestione della Waveform-Audio registrazione

Dopo aver aperto un dispositivo di input audio waveform, è possibile iniziare a registrare i dati audio della forma d'onda. I dati audio waveform vengono registrati in buffer forniti dall'applicazione specificati da una [**struttura WAVEHDR.**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) Questi blocchi di dati devono essere preparati prima di essere usati. Per altre informazioni, vedere [Blocchi di dati audio.](audio-data-blocks.md)

Windows fornisce le funzioni seguenti per gestire la registrazione audio-forma d'onda.



| Funzione                                   | Descrizione                                                                                |
|--------------------------------------------|--------------------------------------------------------------------------------------------|
| [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) | Invia un buffer al driver di dispositivo in modo che possa essere riempito con i dati audio della forma d'onda registrati. |
| [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)         | Arresta la registrazione audio della forma d'onda e contrassegna tutti i buffer in sospeso come fatto.                      |
| [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)         | Avvia la registrazione audio waveform.                                                           |
| [**waveInStop**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)           | Arresta la registrazione audio della forma d'onda.                                                            |



 

Usare la [**funzione waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) per inviare buffer al driver di dispositivo. Poiché i buffer vengono riempiti con dati audio waveform registrati, l'applicazione viene notificata con un messaggio di finestra, un messaggio di callback, un messaggio di thread o un evento, a seconda del flag specificato all'apertura del dispositivo.

Prima di iniziare la registrazione usando [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart), è necessario inviare almeno un buffer al driver. In caso contrario, i dati in ingresso potrebbero andare persi.

Prima di chiudere il dispositivo [**usando waveInClose,**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose)chiamare [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) per contrassegnare tutti i blocchi di dati in sospeso come in corso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione dell'audio Waveform](recording-waveform-audio.md)
</dt> </dl>

 

 