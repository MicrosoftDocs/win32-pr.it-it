---
title: Mappa dei canali
description: Mappa dei canali
ms.assetid: f35d8b76-dfbf-4453-baec-9c0b22f5278a
keywords:
- MidI (Musical Instrument Digital Interface), MIDI Mapper
- MIDI (Musical Instrument Digital Interface),MIDI Mapper
- Mapper MIDI, mappa dei canali
- mappa dei canali
- MIDI Mapper, messaggi del canale
- Messaggi del canale MIDI
- messaggi del canale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d514b5af6df6426db7cc5a313d1c6a52070a49c22a8a04e8cd2a9c34f49d80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688287"
---
# <a name="the-channel-map"></a>Mappa dei canali

La mappa dei canali influisce su tutti i messaggi del canale MIDI. I messaggi del canale MIDI includono i messaggi note-on, note-off, polyphonic-key-aftertouch, control-change, program-change, channel-aftertouch e pitch-curve-change. Midi Mapper usa una singola mappa dei canali con una voce per ognuno dei 16 canali MIDI. Ogni voce della mappa dei canali specifica quanto segue:

-   Canale di destinazione per il messaggio MIDI
-   Un dispositivo di output di destinazione per il messaggio MIDI
-   Mappa di patch facoltativa che specifica altre possibili modifiche per il messaggio MIDI

Il canale di destinazione è impostato su uno dei 16 canali MIDI. I messaggi MIDI vengono modificati in modo da riflettere ogni nuova assegnazione di canale. Ad esempio, se la voce del canale di destinazione per il canale MIDI 4 è impostata su 6, tutti i messaggi MIDI inviati al canale 4 verranno mappati al canale 6, come illustrato nella figura seguente.

![immagine midi mappata](images/mmap-a05.gif)

In questo esempio il byte di stato MIDI 0x93 viene mappato a 0x95. L'ordine basso di un byte di stato MIDI specifica il numero di canale. I canali di origine sono impostati su attivo o inattivo. I messaggi inviati ai canali di origine inattivi vengono ignorati, quindi un canale inattivo viene disattivato o disattivato.

Il dispositivo di output di destinazione è impostato su uno dei dispositivi di output MIDI disponibili. Un dispositivo di output MIDI può essere un sintetizzatore interno o una porta di output MIDI fisica.

I messaggi di sistema MIDI sono messaggi MIDI (con byte di stato) da 0xF0 a 0xFF. Non è presente alcun canale associato ai messaggi di sistema MIDI, pertanto non è possibile eseguire il mapping. I messaggi di sistema MIDI vengono inviati a tutti i dispositivi di output MIDI elencati in una mappa dei canali.

 

 




