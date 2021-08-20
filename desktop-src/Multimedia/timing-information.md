---
title: Informazioni sulla temporizzazione
description: Informazioni sulla temporizzazione
ms.assetid: ff9d6fb2-1387-49ce-a4de-1b2f67353628
keywords:
- MIDI (Musical Instrument Digital Interface), informazioni sulla tempistica
- MIDI (Musical Instrument Digital Interface), informazioni sulla tempistica
- buffer di flusso, informazioni di temporizzazione
- Struttura MIDIEVENT
- buffer di flusso, formato SMPTE
- buffer di flusso,ora nota trimestre
- buffer di flusso, tick
- Formato SMPTE
- ora nota trimestre
- ticks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a75be9964457c64c7c1da59cb93aab2e423f72e861ba496494a5007025461c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804741"
---
# <a name="timing-information"></a>Informazioni sulla temporizzazione

Le informazioni di intervallo per un evento MIDI vengono archiviate nel **membro dwDeltaTime** della [**struttura MIDIEVENT.**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) Il tempo viene specificato in tick, come definito nella *specifica MIDI Files 1.0* standard. La lunghezza di un tick è definita dal formato dell'ora ed eventualmente dal tempo associato al flusso. Per altre informazioni sui flussi, vedere [MIDI Flussi](midi-streams.md).

Un tick viene espresso come microsecondi per ogni nota trimestrale o come tick del tempo SMPTE (Society of Motion Picture and Television Engineers). Le applicazioni che inviano messaggi MIDI singolarmente o usano messaggi MIDI non elaborati usano le informazioni relative al tempo e al tempo per determinare la durata di un tick. Le applicazioni che pre-elaborano i messaggi MIDI possono archiviare il tempo trascorso come conteggio delle unità SMPTE in uso.

L'ora della nota trimestrale è indicata con uno zero nel bit di parola più alto (bit 15) della parola di divisione temporale. Il resto della parola contiene i segni di graduazione per nota trimestrale. Un tempo associato a un flusso di dati MIDI viene mantenuto in unità (microsecondi per trimestre nota) coerenti con la specifica *MIDI Files 1.0* standard. Ad esempio, una nota trimestrale in 4/4 che usa un tempo di 500.000 microsecondi per ogni nota trimestre viene riprodotta alla velocità di 120 battiti al minuto.

I formati di divisione temporale SMPTE specificano completamente la lunghezza di un tick senza la necessità di informazioni sul tempo. Usando i formati di ora SMPTE, le sequenze MIDI possono essere sincronizzate con altri eventi SMPTE, ad esempio video o audio con striped. L'ora SMPTE è indicata con un valore 1 nel bit più alto (bit 15) della parola di divisione temporale. Il resto del byte più significativo specifica il formato SMPTE in uso come valori negativi. I formati SMPTE supportati e i relativi valori corrispondenti (tra parentesi) sono 24 (-24), 25 (-25), 30 (-30) e 30 drop (-29). Il byte basso della parola di divisione temporale specifica il numero di tick per frame SMPTE.

 

 