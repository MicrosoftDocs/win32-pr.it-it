---
title: Architettura del mapper MIDI
description: Architettura del mapper MIDI
ms.assetid: d08d1442-bf9f-46bb-bd44-f512ff4b6bd5
keywords:
- Instrument Digital Interface (MIDI), MIDI Mapper
- MIDI (Instrument Digital Interface), MIDI Mapper
- MIDI Mapper, architettura
- MIDI Mapper, mappa di configurazione
- Mappa di configurazione MIDI
- MIDI Mapper, mappa dei canali
- MIDI Mapper, mappe patch
- MIDI Mapper, mappe delle chiavi
- channel map
- Mappe patch
- mappe delle chiavi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a20e73c9a361487468870698d3c36d59ef35bb6a28da1b03957dd24f1d7b7dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136404"
---
# <a name="the-midi-mapper-architecture"></a>Architettura del mapper MIDI

MidI Mapper usa una mappa di configurazione MIDI per determinare come tradurre e reindirizzare i messaggi ricevuti. Una mappa di configurazione MIDI è costituita dai tipi di mappe seguenti.

-   [Mappa dei canali](the-channel-map.md)
-   [Applicazione di patch Mappe](patch-maps.md)
-   [Chiave Mappe](key-maps.md)

La figura seguente mostra i ruoli delle mappe canale, patch e chiave in una mappa di configurazione MIDI.

![ruoli delle mappe canale, patch e chiave in un'immagine della mappa di configurazione midi](images/mmap-a02.gif)

 

 




