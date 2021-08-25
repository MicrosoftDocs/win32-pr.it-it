---
title: The MIDI Mapper
description: The MIDI Mapper
ms.assetid: 92cffc67-b4a4-4807-94d2-02fbbdba5abf
keywords:
- Windows multimediali, MIDI Mapper
- multimedia,MIDI Mapper
- audio multimediale, mapper MIDI
- audio, mapper MIDI
- Instrument Digital Interface (MIDI), MIDI Mapper
- MIDI (Instrument Digital Interface), MIDI Mapper
- MIDI Mapper,about
- MIDI Mapper, origine
- MIDI Mapper, destinazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a5becc117668964a584f29c311c3e3ac477f672085e837e28d7eecc595658d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805101"
---
# <a name="the-midi-mapper"></a>The MIDI Mapper

I servizi patch standard di MIDI Mapper offrono la riproduzione di file MIDI indipendenti dal dispositivo per le applicazioni. MidI Mapper può essere usato con il sequencer MIDI MCI o con servizi di output MIDI di basso livello.

Se non diversamente specificato, tutti i riferimenti ai numeri di canale MIDI usano i numeri di canale logici da 1 a 16. Questi numeri di canale logici corrispondono ai numeri di canale fisici da 0 a 15 che fanno effettivamente parte del messaggio MIDI. Tutti i riferimenti ai valori di chiave e modifica del programma MIDI usano i valori fisici da 0 a 127. Tutti i numeri sono decimali a meno che non siano preceduti dal prefisso "0x", nel qual caso sono esadecimali.

Nella discussione sul mapper MIDI, il termine *source* si riferisce al lato input del mapper MIDI. Il termine *destinazione* si riferisce al lato di output del mapper MIDI. Ad esempio, un canale di origine è il canale MIDI di un messaggio inviato al mapper MIDI e un canale di destinazione è il canale MIDI di un messaggio inviato dal mapper MIDI a un dispositivo di output.

-   [Mapper MIDI e Windows](the-midi-mapper-and-windows.md)
-   [Architettura del mapper MIDI](the-midi-mapper-architecture.md)
-   [Mappa dei canali](the-channel-map.md)
-   [Applicazione di patch Mappe](patch-maps.md)
-   [Scalare del volume](the-volume-scalar.md)
-   [Chiave Mappe](key-maps.md)
-   [Riepilogo dei Mappe e MIDI](summary-of-maps-and-midi-messages.md)

 

 




