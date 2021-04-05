---
title: Buffer di flusso
description: Buffer di flusso
ms.assetid: d73209a3-4b9d-4405-9e62-8ecfb94c0bd5
keywords:
- Multimedia di Windows, buffer di flusso
- Multimedia, buffer di flusso
- audio multimediale, buffer di flusso
- audio, buffer di flusso
- MIDI (Musical Instrument Digital Interface), buffer di flusso
- MIDI (Musical Instrument Digital Interface), buffer di flusso
- buffer di flusso, informazioni
- Struttura MIDIHDR
- Struttura MIDIEVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d4a01862a8a8e6b7846cbe445737bd13422cf0f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725351"
---
# <a name="stream-buffers"></a>Buffer di flusso

Le applicazioni possono usare i buffer di flusso per inviare flussi di eventi MIDI a un dispositivo. Ogni buffer di flusso è un blocco di memoria a cui punta una struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) . Questo blocco di memoria contiene i dati per uno o più eventi MIDI, ognuno dei quali è definito da una struttura [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) . Un'applicazione controlla il buffer chiamando le funzioni di manipolazione del flusso, ad esempio [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen), [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)e [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose).

-   [Formato del buffer del flusso](stream-buffer-format.md)
-   [Informazioni sull'intervallo](timing-information.md)
-   [Tipi di evento MIDI](midi-event-types.md)
-   [Flussi MIDI](midi-streams.md)

 

 