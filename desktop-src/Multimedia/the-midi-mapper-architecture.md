---
title: Architettura del mapper MIDI
description: Architettura del mapper MIDI
ms.assetid: d08d1442-bf9f-46bb-bd44-f512ff4b6bd5
keywords:
- MIDI (Musical Instrument Digital Interface), Mapper MIDI
- MIDI (Musical Instrument Digital Interface), MIDI Mapper
- Mapper MIDI, architettura
- Mapper MIDI, mappa di installazione
- Mappa di installazione MIDI
- Mapper MIDI, mappa canali
- Mapper MIDI, mappe patch
- Mapper MIDI, mappe chiave
- Mappa canali
- Mappe patch
- Mappe chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba337b05fcff1bd0bb0e948e36e7d290eacb9604
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331567"
---
# <a name="the-midi-mapper-architecture"></a>Architettura del mapper MIDI

Il mapper MIDI usa una mappa di installazione MIDI per determinare come tradurre e reindirizzare i messaggi ricevuti. Una mappa di installazione MIDI è costituita dai tipi di mappe seguenti.

-   [Mappa del canale](the-channel-map.md)
-   [Mappe patch](patch-maps.md)
-   [Mappe chiave](key-maps.md)

Nella figura seguente sono illustrati i ruoli di canale, patch e mappe chiave in una mappa di installazione MIDI.

![ruoli del canale, della patch e delle mappe delle chiavi in un'immagine della mappa di installazione MIDI](images/mmap-a02.gif)

 

 




