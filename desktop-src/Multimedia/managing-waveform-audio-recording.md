---
title: Gestione della registrazione di Waveform-Audio
description: Gestione della registrazione di Waveform-Audio
ms.assetid: a44f7c33-54d6-4ba7-bc57-b63c8b205392
keywords:
- audio Waveform, registrazione
- waveform-interfaccia audio, registrazione
- registrazione dell'audio della forma d'onda, informazioni
- Struttura WAVEHDR
- waveInAddBuffer (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539f722a705d489064d38eccdf6d89e80ccb1518
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336991"
---
# <a name="managing-waveform-audio-recording"></a>Gestione della registrazione di Waveform-Audio

Dopo aver aperto un dispositivo di input audio e di forma d'onda, è possibile iniziare la registrazione dei dati audio della forma d'onda. Forma d'onda: i dati audio vengono registrati nei buffer forniti dall'applicazione specificati da una struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) . È necessario preparare questi blocchi di dati prima di utilizzarli; Per ulteriori informazioni, vedere la pagina relativa ai [blocchi di dati audio](audio-data-blocks.md).

Windows fornisce le funzioni seguenti per gestire la registrazione audio e la forma d'onda.



| Funzione                                   | Descrizione                                                                                |
|--------------------------------------------|--------------------------------------------------------------------------------------------|
| [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) | Invia un buffer al driver di dispositivo in modo che possa essere riempito con i dati audio della forma d'onda registrati. |
| [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)         | Arresta la registrazione audio e di forma d'onda e contrassegna tutti i buffer in sospeso come completato.                      |
| [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)         | Avvia la registrazione audio e la forma d'onda.                                                           |
| [**waveInStop**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)           | Arresta la registrazione audio e la forma d'onda.                                                            |



 

Usare la funzione [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) per inviare i buffer al driver di dispositivo. Quando i buffer sono riempiti con dati audio e di forma d'onda registrati, l'applicazione riceve una notifica con un messaggio di finestra, un messaggio di callback, un messaggio di thread o un evento, a seconda del flag specificato quando il dispositivo è stato aperto.

Prima di iniziare la registrazione tramite [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart), è necessario inviare almeno un buffer al driver oppure i dati in arrivo potrebbero andare persi.

Prima di chiudere il dispositivo usando [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose), chiamare [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) per contrassegnare eventuali blocchi di dati in sospeso come eseguiti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione dell'audio della forma d'onda](recording-waveform-audio.md)
</dt> </dl>

 

 