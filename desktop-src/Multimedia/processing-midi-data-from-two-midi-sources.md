---
title: Elaborazione di dati MIDI da due origini MIDI
description: Elaborazione di dati MIDI da due origini MIDI
ms.assetid: d8b605d9-a12a-4830-8f29-ea700aefb41d
keywords:
- Multimedia di Windows, elaborazione di dati MIDI da due origini
- Multimedia, elaborazione di dati MIDI da due origini
- audio multimediale, elaborazione di dati MIDI da due origini
- audio, elaborazione di dati MIDI da due origini
- MIDI (Musical Instrument Digital Interface), elaborazione di dati da due origini
- MIDI (Musical Instrument Digital Interface), elaborazione di dati da due origini
- elaborazione di dati MIDI da due origini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513dcd16036f6f833aec6813f75c6c082925f666
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046678"
---
# <a name="processing-midi-data-from-two-midi-sources"></a>Elaborazione di dati MIDI da due origini MIDI

Il sottosistema MIDI può instradare i messaggi MIDI da due origini dati a un singolo dispositivo di output MIDI per la riproduzione simultanea. Ad esempio, un'origine può essere musica in background o una linea di basso che è stata pre-registrata e memorizzata in un file. La seconda origine può essere costituita da dati dinamici da uno strumento MIDI, ad esempio una tastiera o una chitarra.

Entrambe le origini dati inviano i dati MIDI a un singolo dispositivo MIDI identificato con un handle. Inviare un flusso di dati tramite la funzione [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) e uno o più buffer di flusso. Questo flusso di dati contiene in genere dati preregistrati che vengono compressi nel buffer.

Inviare in modo asincrono il secondo flusso di dati, in genere da uno strumento MIDI, usando la funzione [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) . Lo stato di esecuzione di un buffer del flusso non verrà influenzato negativamente dalle chiamate asincrone effettuate dal secondo flusso di dati.

Ogni breve messaggio inviato con **midiOutShortMsg** deve essere un messaggio MIDI completo, con un byte di stato e il numero appropriato di byte di dati. Se il byte di stato viene omesso, **midiOutShortMsg** restituisce un errore. (Tuttavia, non è presente alcuno stato di esecuzione con l'output del flusso).

 

 