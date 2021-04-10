---
title: Mappe chiave
description: Mappe chiave
ms.assetid: 5d0367b0-bbf1-4a4b-98b2-dbca6f2f8b0c
keywords:
- MIDI (Musical Instrument Digital Interface), Mapper MIDI
- MIDI (Musical Instrument Digital Interface), MIDI Mapper
- Mapper MIDI, mappe chiave
- Mappe chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffafd99e6d813f12c388b633997980b7a58d62dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955321"
---
# <a name="key-maps"></a>Mappe chiave

Ogni voce nella tabella di traduzione della mappa patch può avere una mappa delle chiavi associata. Le mappe chiave influiscono sui messaggi note-on, note-off e polifoniche-Key-aftertouch. Una mappa delle chiavi include una tabella di traduzione con una voce per ogni valore di chiave MIDI 128. Se, ad esempio, la voce relativa al valore della chiave 60 è 72, il mapper MIDI modifica i messaggi di note MIDI su, come illustrato nella figura seguente.

![immagine del mapper MIDI](images/mmap-a06.gif)

Le mappe chiave sono utili con i sintetizzatori che hanno strumenti di percussione basati su chiavi con un suono di percussione particolare assegnato a ogni chiave. Le mappe chiave vengono in genere assegnate alla prima patch nelle mappe delle patch nei canali di percussione (10 e 16).

 

 




