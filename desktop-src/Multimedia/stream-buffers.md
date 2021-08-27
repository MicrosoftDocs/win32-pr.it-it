---
title: Buffer di flusso
description: Buffer di flusso
ms.assetid: d73209a3-4b9d-4405-9e62-8ecfb94c0bd5
keywords:
- Windows multimediali, buffer di flusso
- multimediali, buffer di flusso
- audio multimediale, buffer di flusso
- audio, buffer di flusso
- MIDI (Musical Instrument Digital Interface), buffer di flusso
- MIDI (Musical Instrument Digital Interface), buffer di flusso
- buffer di flusso, informazioni
- Struttura MIDIHDR
- Struttura MIDIEVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac10d024089a856880097c5d87ae501d62655f858030535ff4128f1fd9d31447
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037071"
---
# <a name="stream-buffers"></a>Buffer di flusso

Le applicazioni possono usare buffer di flusso per inviare flussi di eventi MIDI a un dispositivo. Ogni buffer di flusso è un blocco di memoria a cui punta [**una struttura MIDIHDR.**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) Questo blocco di memoria contiene dati per uno o più eventi MIDI, ognuno dei quali è definito da [**una struttura MIDIEVENT.**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) Un'applicazione controlla il buffer chiamando le funzioni di manipolazione del flusso, ad esempio [**midiStreamOpen,**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen) [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)e [**midiStreamClose.**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)

-   [Formato buffer di flusso](stream-buffer-format.md)
-   [Informazioni sulla temporizzazione](timing-information.md)
-   [Tipi di evento MIDI](midi-event-types.md)
-   [Midi Flussi](midi-streams.md)

 

 