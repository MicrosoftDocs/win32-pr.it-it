---
title: Uso di una finestra o di un thread per gestire la riproduzione memorizzata nel buffer
description: Uso di una finestra o di un thread per gestire la riproduzione memorizzata nel buffer
ms.assetid: 3c8145a8-e56a-449d-ad45-2ae016f79697
keywords:
- Instrument Digital Interface (MIDI), riproduzione memorizzata nel buffer
- MIDI (Instrument Digital Interface), riproduzione memorizzata nel buffer
- riproduzione di file MIDI, riproduzione memorizzata nel buffer
- riproduzione memorizzata nel buffer
- MM_MOM_CLOSE messaggio
- MM_MOM_DONE messaggio
- MM_MOM_OPEN messaggio
- Instrument Digital Interface (MIDI), invio di messaggi
- MIDI (Instrument Digital Interface), invio di messaggi
- riproduzione di file MIDI, invio di messaggi
- invio di messaggi MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc0acb39090a640d60539542a439111287faef246adf64aef7ee12ced3ae09e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801255"
---
# <a name="using-a-window-or-thread-to-manage-buffered-playback"></a>Uso di una finestra o di un thread per gestire la riproduzione memorizzata nel buffer

I messaggi seguenti possono essere inviati a una finestra o a un thread per la gestione della riproduzione di messaggi o buffer di flusso esclusivi di sistema MIDI.



| Valore                                  | Significato                                                                                                                                                                  |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ MOM \_ CLOSE**](mm-mom-close.md) | Inviato quando il dispositivo viene chiuso usando la [**funzione midiOutClose.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose)                                                                               |
| [**MM \_ MOM \_ DONE**](mm-mom-done.md)   | Inviato quando il driver di dispositivo termina con un blocco di dati inviato tramite la [**funzione midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) [**o midiStreamOut.**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) |
| [**MM \_ MOM \_ OPEN**](mm-mom-open.md)   | Inviato quando il dispositivo viene aperto usando la [**funzione midiOutOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)                                                                                 |



 

A ognuno di questi messaggi sono associati un parametro *wParam* e un parametro *lParam.* Il *parametro wParam* specifica sempre l'handle di un dispositivo MIDI aperto. Per [**MM \_ MOM \_ DONE**](mm-mom-done.md), *lParam* specifica un indirizzo di una [**struttura MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) che identifica il blocco di dati completato. Il *parametro lParam* non è usato per [**MM MOM \_ \_ CLOSE**](mm-mom-close.md) e [**MM MOM \_ \_ OPEN.**](mm-mom-open.md)

Il messaggio più utile è probabilmente MM \_ MOM \_ DONE. A meno che non sia necessario allocare memoria o inizializzare variabili, probabilmente non è necessario elaborare MM \_ MOM OPEN e MM MOM \_ \_ \_ CLOSE. Al termine della riproduzione di un blocco di dati, è possibile pulire e liberare il blocco di dati.

 

 