---
title: Uso di una finestra o di un thread per gestire la riproduzione memorizzata nel buffer
description: Uso di una finestra o di un thread per gestire la riproduzione memorizzata nel buffer
ms.assetid: 3c8145a8-e56a-449d-ad45-2ae016f79697
keywords:
- MIDI (Musical Instrument Digital Interface), riproduzione memorizzata nel buffer
- MIDI (Musical Instrument Digital Interface), riproduzione memorizzata nel buffer
- riproduzione di file MIDI, riproduzione memorizzata nel buffer
- riproduzione memorizzata nel buffer
- Messaggio MM_MOM_CLOSE
- Messaggio MM_MOM_DONE
- Messaggio MM_MOM_OPEN
- MIDI (Musical Instrument Digital Interface), invio di messaggi
- MIDI (Musical Instrument Digital Interface), invio di messaggi
- riproduzione di file MIDI, invio di messaggi
- invio di messaggi MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c8c120504a4a25ddcf01474db341a367a2e9854
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337311"
---
# <a name="using-a-window-or-thread-to-manage-buffered-playback"></a>Uso di una finestra o di un thread per gestire la riproduzione memorizzata nel buffer

I messaggi seguenti possono essere inviati a una finestra o a un thread per la gestione della riproduzione dei messaggi esclusivi del sistema MIDI o dei buffer di flusso.



| Valore                                  | Significato                                                                                                                                                                  |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ \_ chiusura MOM**](mm-mom-close.md) | Inviato quando il dispositivo viene chiuso tramite la funzione [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) .                                                                               |
| [**MM \_ MOM \_ completato**](mm-mom-done.md)   | Inviato quando il driver di dispositivo viene terminato con un blocco di dati inviato tramite la funzione [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) o [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) . |
| [**MM- \_ MOM \_ aperto**](mm-mom-open.md)   | Inviato quando il dispositivo viene aperto tramite la funzione [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .                                                                                 |



 

Un parametro *wParam* e un parametro *lParam* sono associati a ognuno di questi messaggi. Il parametro *wParam* specifica sempre l'handle di un dispositivo MIDI aperto. Per [**\_ MOM mm \_ done**](mm-mom-done.md), *lParam* specifica un indirizzo di una struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) che identifica il blocco di dati completato. Il parametro *lParam* non è usato per [**la \_ \_ chiusura MOM di mm**](mm-mom-close.md) e la [**\_ MOM \_ aperta**](mm-mom-open.md).

Il messaggio più utile è probabilmente MM \_ MOM \_ done. A meno che non sia necessario allocare memoria o inizializzare variabili, è probabile che non sia necessario elaborare MM \_ MOM \_ Open e mm \_ MOM \_ Close. Quando viene completata la riproduzione di un blocco di dati, è possibile pulire e liberare il blocco di dati.

 

 