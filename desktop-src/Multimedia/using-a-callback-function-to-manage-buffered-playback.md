---
title: Utilizzo di una funzione di callback per gestire la riproduzione memorizzata nel buffer
description: Utilizzo di una funzione di callback per gestire la riproduzione memorizzata nel buffer
ms.assetid: aaaf9c5f-c9b2-4e55-a4c1-28c99cc03945
keywords:
- MIDI (Musical Instrument Digital Interface), riproduzione memorizzata nel buffer
- MIDI (Musical Instrument Digital Interface), riproduzione memorizzata nel buffer
- riproduzione di file MIDI, riproduzione memorizzata nel buffer
- riproduzione memorizzata nel buffer
- Messaggio MOM_CLOSE
- Messaggio MOM_DONE
- Messaggio MOM_OPEN
- MIDI (Musical Instrument Digital Interface), invio di messaggi
- MIDI (Musical Instrument Digital Interface), invio di messaggi
- riproduzione di file MIDI, invio di messaggi
- invio di messaggi MIDI
- MIDI (Musical Instrument Digital Interface), funzioni di callback
- MIDI (Musical Instrument Digital Interface), funzioni di callback
- riproduzione di file MIDI, funzioni di callback
- Funzione di callback MidiOutProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bccccd8e5fb052b89e8ca1804b89de6da26cd5b7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726295"
---
# <a name="using-a-callback-function-to-manage-buffered-playback"></a>Utilizzo di una funzione di callback per gestire la riproduzione memorizzata nel buffer

È possibile definire una funzione di callback personalizzata per gestire la riproduzione del buffer dei dispositivi di output MIDI. La funzione di callback è documentata come [**MidiOutProc**](/previous-versions//dd798478(v=vs.85)).

I messaggi seguenti possono essere inviati al parametro *wmsg* della funzione di callback **MidiOutProc** .



| Valore                           | Significato                                                                                                                                                                  |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_chiusura MOM**](mom-close.md) | Inviato quando il dispositivo viene chiuso tramite la funzione [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) .                                                                               |
| [**MOM \_ completato**](mom-done.md)   | Inviato quando il driver di dispositivo viene terminato con un blocco di dati inviato tramite la funzione [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) o [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) . |
| [**MOM \_ aperto**](mom-open.md)   | Inviato quando il dispositivo viene aperto tramite la funzione [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .                                                                                 |



 

Questi messaggi sono simili a quelli inviati alle funzioni di routine della finestra, ma i parametri sono diversi. Un handle del dispositivo MIDI aperto viene passato come parametro alla funzione di callback, insieme al parola doppia dei dati dell'istanza passati usando **midiOutOpen**.

Al termine del driver, è possibile pulire e liberare il blocco di dati. A causa delle restrizioni suggerite sulle funzioni di callback, è preferibile non eseguire questa operazione dall'interno della funzione di callback.

 

 