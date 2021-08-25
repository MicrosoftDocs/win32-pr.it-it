---
title: Elaborazione di dati MIDI da due origini MIDI
description: Elaborazione di dati MIDI da due origini MIDI
ms.assetid: d8b605d9-a12a-4830-8f29-ea700aefb41d
keywords:
- Windows multimediali, elaborazione di dati MIDI da due origini
- multimediali, elaborazione di dati MIDI da due origini
- audio multimediale, elaborazione di dati MIDI da due origini
- audio, elaborazione di dati MIDI da due origini
- Instrument Digital Interface (MIDI), elaborazione di dati da due origini
- MIDI (Instrument Digital Interface), elaborazione di dati da due origini
- elaborazione di dati MIDI da due origini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a5eb31c4c6b4b965321b7458d058a3547426b95236d6e0b52d6eb0f55b3e74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805791"
---
# <a name="processing-midi-data-from-two-midi-sources"></a>Elaborazione di dati MIDI da due origini MIDI

Il sottosistema MIDI può indirizzare i messaggi MIDI da due origini dati a un singolo dispositivo di output MIDI per la riproduzione simultanea. Ad esempio, un'origine può essere musica di sottofondo o linea di base preregistrata e archiviata in un file. La seconda origine può essere dati in tempo reale da uno strumento MIDI, ad esempio una tastiera o una tastiera.

Entrambe le origini dati inviano i dati MIDI a un singolo dispositivo MIDI identificato con un handle. Inviare un flusso di dati usando [**la funzione midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) e uno o più buffer di flusso. Questo flusso di dati contiene in genere dati preregistrati che vengono memorizzati nel buffer.

Inviare il secondo flusso di dati (in genere da uno strumento MIDI) in modo asincrono usando la [**funzione midiOutShortMsg.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) Lo stato di esecuzione di un buffer del flusso non sarà influenzato negativamente dalle chiamate asincrone effettuate dal secondo flusso di dati.

Ogni messaggio breve inviato con **midiOutShortMsg** deve essere un messaggio MIDI completo, con un byte di stato e il numero appropriato di byte di dati. Se il byte di stato viene omesso, **midiOutShortMsg** restituisce un errore. Non esiste tuttavia alcuno stato di esecuzione con l'output del flusso.

 

 