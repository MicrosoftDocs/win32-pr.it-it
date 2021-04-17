---
title: Invio di singoli messaggi MIDI
description: Invio di singoli messaggi MIDI
ms.assetid: 9e5b7194-d6d0-40a6-b8c1-ea9442f34bd8
keywords:
- MIDI (Musical Instrument Digital Interface), invio di messaggi
- MIDI (Musical Instrument Digital Interface), invio di messaggi
- riproduzione di file MIDI, invio di messaggi
- invio di messaggi MIDI
- MIDI (Musical Instrument Digital Interface), singoli messaggi
- MIDI (Musical Instrument Digital Interface), singoli messaggi
- riproduzione di file MIDI, singoli messaggi
- singoli messaggi MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5473d1ab7361c26a922683ed7d5021995b0f13ea
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299656"
---
# <a name="sending-individual-midi-messages"></a>Invio di singoli messaggi MIDI

È possibile utilizzare i singoli messaggi MIDI utilizzando le funzioni seguenti.



| Valore                                      | Significato                                                                                                                                                                             |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)   | Invia un buffer di dati MIDI al dispositivo di output MIDI specificato. Usare questa funzione per inviare messaggi esclusivi del sistema a un dispositivo MIDI.                                              |
| [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)       | Disattiva tutte le note in tutti i canali per un dispositivo di output MIDI specificato. I buffer di flusso e i buffer esclusivi del sistema in sospeso sono contrassegnati come done e restituiti all'applicazione. |
| [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) | Invia un messaggio MIDI a un dispositivo di output MIDI specificato.                                                                                                                             |



 

Per inviare qualsiasi messaggio MIDI (ad eccezione dei messaggi di sistema esclusivi), usare [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg).

 

 