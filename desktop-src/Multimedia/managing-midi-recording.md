---
title: Gestione della registrazione MIDI
description: Gestione della registrazione MIDI
ms.assetid: 48b2d815-72cf-4c96-8d93-247d2426b8f2
keywords:
- Strumentazione musicale Digital Interface (MIDI), registrazione
- MIDI (Musical Instrument Digital Interface), registrazione
- registrazione di audio MIDI, gestione
- Registrazione MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29bf4ac85ad0cc9735a08bab3ee07d744eecb0d75308ee323ec93c1c69b1a9e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139062"
---
# <a name="managing-midi-recording"></a>Gestione della registrazione MIDI

Dopo aver aperto un dispositivo MIDI, è possibile iniziare a registrare i dati MIDI. Windows fornisce le funzioni seguenti per la gestione della registrazione MIDI.



| Valore                                      | Significato                                                                                           |
|--------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) | Invia un buffer al driver di dispositivo in modo che possa essere riempito con dati MIDI esclusivi del sistema registrati. |
| [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)         | Arresta la registrazione MIDI e contrassegna tutti i buffer in sospeso come completata.                                       |
| [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)         | Avvia la registrazione MIDI e reimposta il timestamp su zero.                                          |
| [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)           | Arresta la registrazione MIDI.                                                                             |



 

Per inviare buffer al driver di dispositivo per la registrazione di messaggi esclusivi di sistema, [**usare midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer). L'applicazione viene notificata quando i buffer vengono riempiti con dati registrati esclusivi del sistema. Per altre informazioni sulle tecniche di notifica, vedere [Gestione dei blocchi di dati MIDI.](managing-midi-data-blocks.md)

La [**funzione midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) avvia il processo di registrazione. Quando si registrano messaggi esclusivi di sistema, inviare almeno un buffer al driver prima di avviare la registrazione. Per arrestare la registrazione, [**usare midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop). Prima di chiudere il dispositivo usando la [**funzione midiInClose,**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) contrassegnare tutti i blocchi di dati in sospeso come eseguiti [**chiamando midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset).

Le applicazioni che richiedono dati con timestamp usano una funzione di callback per ricevere dati MIDI. Se i requisiti di temporizzazione non sono rigorosi, è possibile usare un callback di finestra o thread. Tuttavia, non è possibile usare un callback di evento per ricevere dati MIDI.

Per registrare i messaggi esclusivi di sistema con applicazioni che non usano buffer di flusso, è necessario fornire i buffer al driver di dispositivo. Questi buffer vengono specificati usando una [**struttura MIDIHDR.**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione dell'audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 