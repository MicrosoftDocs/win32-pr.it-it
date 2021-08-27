---
title: Invio di singoli messaggi MIDI
description: Invio di singoli messaggi MIDI
ms.assetid: 9e5b7194-d6d0-40a6-b8c1-ea9442f34bd8
keywords:
- Instrument Digital Interface (MIDI), invio di messaggi
- MIDI (Instrument Digital Interface), invio di messaggi
- riproduzione di file MIDI, invio di messaggi
- invio di messaggi MIDI
- Instrument Digital Interface (MIDI), singoli messaggi
- MIDI (Instrument Digital Interface), singoli messaggi
- riproduzione di file MIDI, singoli messaggi
- singoli messaggi MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d1f73d0956004f90644ce2e8b0e41b368137a7b61fd04e6d17302619980336d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037451"
---
# <a name="sending-individual-midi-messages"></a>Invio di singoli messaggi MIDI

È possibile usare singoli messaggi MIDI usando le funzioni seguenti.



| Valore                                      | Significato                                                                                                                                                                             |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)   | Invia un buffer di dati MIDI al dispositivo di output MIDI specificato. Usare questa funzione per inviare messaggi esclusivi di sistema a un dispositivo MIDI.                                              |
| [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)       | Disattiva tutte le note su tutti i canali per un dispositivo di output MIDI specificato. Tutti i buffer esclusivi del sistema in sospeso e i buffer di flusso vengono contrassegnati come completata e restituiti all'applicazione. |
| [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) | Invia un messaggio MIDI a un dispositivo di output MIDI specificato.                                                                                                                             |



 

Per inviare qualsiasi messaggio MIDI (ad eccezione dei messaggi esclusivi del sistema), usare [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg).

 

 