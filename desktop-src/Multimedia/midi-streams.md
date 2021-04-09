---
title: Flussi MIDI
description: Flussi MIDI
ms.assetid: 622472d9-2888-407f-bdaa-4943896c0bac
keywords:
- MIDI (Musical Instrument Digital Interface), flussi
- MIDI (Musical Instrument Digital Interface), flussi
- buffer di flusso, flussi MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4237e1590f3af2e15a3b0b9fedea2fea4c9c40fc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117706"
---
# <a name="midi-streams"></a>Flussi MIDI

Gli eventi MIDI si verificano nel contesto di un flusso di dati MIDI. Sebbene un'applicazione possa usare diversi flussi per definire i dati musicali, il mapper MIDI non riconosce più flussi. Per la maggior parte delle applicazioni che usano flussi viene usato un solo flusso MIDI.

Le funzioni seguenti funzionano con i flussi.



| Valore                                            | Significato                                                                 |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)       | Chiude un flusso MIDI.                                                   |
| [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)         | Apre un flusso MIDI e recupera un handle.                             |
| [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)           | Riproduce o Accoda un flusso (buffer) di dati MIDI a un dispositivo di output MIDI. |
| [**midiStreamPause**](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)       | Sospende la riproduzione di un flusso MIDI specificato.                             |
| [**midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) | Recupera la posizione corrente in un flusso MIDI.                        |
| [**midiStreamProperty**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty) | Imposta e recupera le proprietà del flusso.                                   |
| [**midiStreamRestart**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)   | Riavvia la riproduzione di un flusso MIDI sospeso.                              |
| [**midiStreamStop**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)         | Disattiva tutte le note in tutti i canali MIDI per il flusso MIDI specificato. |



 

 

 