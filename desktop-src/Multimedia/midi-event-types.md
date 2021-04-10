---
title: Tipi di evento MIDI
description: Tipi di evento MIDI
ms.assetid: 0b0984b7-3087-461e-90f2-a899dc1a88c6
keywords:
- MIDI (Musical Instrument Digital Interface), tipi di evento
- MIDI (Musical Instrument Digital Interface), tipi di evento
- Struttura MIDIEVENT
- buffer di flusso, tipi di evento MIDI
- Tipi di evento MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 823ce5ce7af898ca3178e0379fb814c54fbf06b7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046723"
---
# <a name="midi-event-types"></a>Tipi di evento MIDI

Il membro **dwEvent** della struttura [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) descrive l'evento MIDI che deve essere eseguita. Gli eventi brevi si adattano interamente a questo membro. Per gli eventi Long sono necessari uno o più valori parola doppia oltre al membro **dwEvent** per archiviare le descrizioni degli eventi.

Il byte elevato del membro **dwEvent** contiene informazioni sul fatto che l'evento sia lungo o breve e che venga generato un callback insieme all'evento. Questo byte viene inoltre usato per descrivere il tipo di evento. I restanti 24 bit del membro **dwEvent** vengono utilizzati per contenere i parametri evento (per i messaggi brevi) o per contenere la lunghezza dei parametri evento (per i messaggi lunghi). Per estrarre informazioni dal membro **dwEvent** , usare le macro [**MEVT \_ eventType**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype) e [**MEVT \_ EVENTPARM**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm) .

Per una descrizione dei tipi di evento predefiniti, vedere il materiale di riferimento per la struttura **MIDIEVENT** .

 

 