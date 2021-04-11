---
title: Mapper MIDI
description: Mapper MIDI
ms.assetid: 92cffc67-b4a4-4807-94d2-02fbbdba5abf
keywords:
- Windows Multimedia, Mapper MIDI
- Multimedia, Mapper MIDI
- audio multimediale, Mapper MIDI
- audio, Mapper MIDI
- MIDI (Musical Instrument Digital Interface), Mapper MIDI
- MIDI (Musical Instrument Digital Interface), MIDI Mapper
- Mapper MIDI, informazioni
- Mapper MIDI, origine
- Mapper MIDI, destinazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b360148c994c0ee6434fdf097ca5f393b23d49
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044540"
---
# <a name="the-midi-mapper"></a>Mapper MIDI

I servizi patch standard del mapper MIDI forniscono la riproduzione dei file MIDI indipendenti dal dispositivo per le applicazioni. Il mapper MIDI può essere usato con il sequencer MIDI di MCI o con servizi di output MIDI di basso livello.

Se non specificato diversamente, tutti i riferimenti ai numeri di canale MIDI utilizzano i numeri di canale logico da 1 a 16. Questi numeri di canale logico corrispondono ai numeri di canale fisico da 0 a 15 che fanno effettivamente parte del messaggio MIDI. Tutti i riferimenti ai valori delle chiavi e delle modifiche dei programmi MIDI usano i valori fisici da 0 a 127. Tutti i numeri sono decimali, a meno che non siano preceduti dal prefisso "0x", nel qual caso sono esadecimali.

Nella discussione del mapper MIDI, il termine *origine* si riferisce al lato di input del mapper MIDI. Il termine *destinazione* si riferisce al lato output del mapper MIDI. Un canale di origine, ad esempio, è il canale MIDI di un messaggio inviato al mapper MIDI e un canale di destinazione è il canale MIDI di un messaggio inviato dal mapper MIDI a un dispositivo di output.

-   [Il mapper MIDI e Windows](the-midi-mapper-and-windows.md)
-   [Architettura del mapper MIDI](the-midi-mapper-architecture.md)
-   [Mappa del canale](the-channel-map.md)
-   [Mappe patch](patch-maps.md)
-   [Volume scalare](the-volume-scalar.md)
-   [Mappe chiave](key-maps.md)
-   [Riepilogo delle mappe e dei messaggi MIDI](summary-of-maps-and-midi-messages.md)

 

 




