---
title: Informazioni sull'intervallo
description: Informazioni sull'intervallo
ms.assetid: ff9d6fb2-1387-49ce-a4de-1b2f67353628
keywords:
- MIDI (Musical Instrument Digital Interface), informazioni sugli intervalli
- MIDI (Musical Instrument Digital Interface), informazioni sugli intervalli
- buffer di flusso, informazioni sugli intervalli
- Struttura MIDIEVENT
- buffer di flusso, formato SMPTE
- buffer di flusso, ora della nota trimestre
- buffer di flusso, cicli
- Formato SMPTE
- ora della nota trimestre
- ticks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2daf5b1847456e8fb518665521e484118fead79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117599"
---
# <a name="timing-information"></a>Informazioni sull'intervallo

Le informazioni di temporizzazione per un evento MIDI vengono archiviate nel membro **dwDeltaTime** della struttura [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) . Il tempo è espresso in cicli, come definito nella specifica dei *file MIDI Standard 1,0* . La lunghezza di un segno di selezione è definita dal formato dell'ora e possibilmente dal tempo associato al flusso. Per altre informazioni sui flussi, vedere [flussi MIDI](midi-streams.md).

Un segno di ingrandimento è espresso in microsecondi per ogni trimestre o come segni di cadenza del periodo di tempo. Le applicazioni che inviano messaggi MIDI singolarmente o usano messaggi MIDI non elaborati usano le informazioni relative a tempo e tempo per la nota del trimestre per determinare la durata di un segno di cadenza. Le applicazioni che preelaborano i messaggi MIDI possono archiviare il tempo trascorso come un conteggio delle unità SMPTE utilizzate.

La durata della nota di trimestre è indicata da uno zero nel bit a parola alta (bit 15) della parola di divisione temporale. Il resto della parola contiene la nota relativa ai cicli per trimestre. Un tempo associato a un flusso di dati MIDI viene mantenuto in unità (in microsecondi per ogni trimestre) coerente con la specifica dei *file MIDI Standard 1,0* . Ad esempio, una nota di trimestre in 4/4 di tempo che usa un tempo di 500.000 microsecondi per ogni trimestre viene riprodotta alla velocità di 120 battute al minuto.

I formati della divisione temporale SMPTE specificano completamente la lunghezza di un segno di incirca senza la necessità di informazioni sul tempo. Quando si usano i formati di ora SMPTE, le sequenze MIDI possono essere sincronizzate con altri eventi SMPTE, ad esempio video o audio con striping. Il tempo SMPTE è indicato con un valore 1 nel bit più significativo (bit 15) della parola di divisione temporale. Il resto del byte più significativo specifica il formato SMPTE in uso come valore negativo. I formati SMPTE supportati e i valori corrispondenti (tra parentesi) sono 24 (-24), 25 (-25), 30 (-30) e 30 drop (-29). Il byte inferiore della parola di divisione temporale specifica il numero di cicli per fotogramma SMPTE.

 

 