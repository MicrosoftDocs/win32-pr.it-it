---
title: Midi Flussi
description: Midi Flussi
ms.assetid: 622472d9-2888-407f-bdaa-4943896c0bac
keywords:
- MIDI (Musical Instrument Digital Interface), streams
- MIDI (Musical Instrument Digital Interface),streams
- buffer di flusso, flussi MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d06f1203fb8ab2a5bd1cdba69b11df99bab72b3f873c49c53da14ea61c6a6cdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802841"
---
# <a name="midi-streams"></a>Midi Flussi

Gli eventi MIDI si verificano nel contesto di un flusso di dati MIDI. Anche se un'applicazione può usare diversi flussi per definire dati musicali, il mapper MIDI non riconosce più flussi. La maggior parte delle applicazioni che usano flussi usa un singolo flusso MIDI.

Le funzioni seguenti funzionano con i flussi.



| Valore                                            | Significato                                                                 |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)       | Chiude un flusso MIDI.                                                   |
| [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)         | Apre un flusso MIDI e recupera un handle.                             |
| [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)           | Riproduce o accoda un flusso (buffer) di dati MIDI a un dispositivo di output MIDI. |
| [**midiStreamPause**](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)       | Sospende la riproduzione di un flusso MIDI specificato.                             |
| [**midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) | Recupera la posizione corrente in un flusso MIDI.                        |
| [**midiStreamProperty**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty) | Imposta e recupera le proprietà del flusso.                                   |
| [**midiStreamRestart**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)   | Riavvia la riproduzione di un flusso MIDI sospeso.                              |
| [**midiStreamStop**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)         | Disattiva tutte le note su tutti i canali MIDI per il flusso MIDI specificato. |



 

 

 