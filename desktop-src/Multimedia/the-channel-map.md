---
title: Mappa del canale
description: Mappa del canale
ms.assetid: f35d8b76-dfbf-4453-baec-9c0b22f5278a
keywords:
- MIDI (Musical Instrument Digital Interface), Mapper MIDI
- MIDI (Musical Instrument Digital Interface), MIDI Mapper
- Mapper MIDI, mappa canali
- Mappa canali
- Mapper MIDI, messaggi del canale
- Messaggi del canale MIDI
- messaggi del canale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87027c74ebddea9b51545d15bfa90e52dee95a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116868"
---
# <a name="the-channel-map"></a>Mappa del canale

La mappa del canale influiscono su tutti i messaggi del canale MIDI. I messaggi del canale MIDI includono i messaggi note-on, note-off, polifoniche-Key-aftertouch, CTRL-Change, Program-Change, Channel-aftertouch e Pitch-Bend-Change. Il mapper MIDI usa una singola mappa del canale con una voce per ognuno dei 16 canali MIDI. Ogni voce della mappa del canale specifica quanto segue:

-   Canale di destinazione per il messaggio MIDI
-   Un dispositivo di output di destinazione per il messaggio MIDI
-   Mappa patch facoltativa che specifica altre possibili modifiche per il messaggio MIDI

Il canale di destinazione è impostato su uno dei 16 canali MIDI. I messaggi MIDI vengono modificati in modo da riflettere ogni nuova assegnazione del canale. Se, ad esempio, la voce del canale di destinazione per il canale MIDI 4 è impostata su 6, viene eseguito il mapping di tutti i messaggi MIDI inviati a Channel 4 a Channel 6, come illustrato nella figura seguente.

![immagine MIDI mappata](images/mmap-a05.gif)

In questo esempio il byte di stato MIDI 0x93 viene mappato a 0x95. L'ordine inferiore di un byte di stato MIDI specifica il numero del canale. I canali di origine sono impostati su attivo o inattivo. I messaggi inviati ai canali di origine inattivi vengono ignorati, pertanto un canale inattivo viene attivato o disattivato.

Il dispositivo di output di destinazione è impostato su uno dei dispositivi di output MIDI disponibili. Un dispositivo di output MIDI può essere un sintetizzatore interno o una porta di output MIDI fisica.

I messaggi di sistema MIDI sono messaggi MIDI (con byte di stato) da 0xF0 a 0xFF. Non esiste alcun canale associato ai messaggi di sistema MIDI, pertanto non è possibile eseguirne il mapping. I messaggi di sistema MIDI vengono inviati a tutti i dispositivi di output MIDI elencati in una mappa canali.

 

 




